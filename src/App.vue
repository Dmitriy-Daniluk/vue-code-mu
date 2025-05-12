<template>
	<div>
		<h1>Блокнот</h1>

		<div class="notebook">
			<div class="menu">
				<h2>Записи</h2>
				<ul>
					<li v-for="(note, index) in filteredNotes" :key="note.id">
						<button @click="selectNote(index)">
							{{ note.title }}
						</button>
						<button @click="removeNote(index)">Удалить</button>
					</li>
				</ul>
				<input v-model="searchQuery" placeholder="Поиск..." />
			</div>

			<div class="editor">
				<h2>Редактировать запись</h2>
				<textarea v-model="currentNote.text" placeholder="Напишите что-то..."></textarea>
				<button @click="saveNote">Сохранить</button>
			</div>
		</div>

		<button @click="addNote">Добавить новую запись</button>
	</div>
</template>

<script>
export default {
	data() {
		return {
			notes: [],
			currentNote: { title: '', text: '' },
			searchQuery: '',
		};
	},
	computed: {
		filteredNotes() {
			return this.notes.filter(note =>
				note.title.toLowerCase().includes(this.searchQuery.toLowerCase())
			);
		},
	},
	methods: {
		addNote() {
			const newNote = { id: Date.now(), title: `Запись ${this.notes.length + 1}`, text: '' };
			this.notes.push(newNote);
			this.selectNote(this.notes.length - 1);
		},
		selectNote(index) {
			this.currentNote = { ...this.notes[index] };
		},
		saveNote() {
			const index = this.notes.findIndex(note => note.id === this.currentNote.id);
			if (index !== -1) {
				this.notes[index] = { ...this.currentNote };
			}
		},
		removeNote(index) {
			this.notes.splice(index, 1);
			if (this.notes.length > 0) {
				this.selectNote(0);
			} else {
				this.currentNote = { title: '', text: '' };
			}
		},
	},
};
</script>

<style>
.notebook {
	display: flex;
	justify-content: space-between;
}

.menu {
	width: 200px;
}

.editor {
	width: 300px;
}

textarea {
	width: 100%;
	height: 200px;
}

button {
	margin-top: 10px;
}
</style>
