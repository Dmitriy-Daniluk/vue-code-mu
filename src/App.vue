<template>
	<div>
		<!-- Задание 1: Добавление в конец массива -->
		<input v-model="newItem" />
		<button @click="addItem">Add</button>

		<ul>
			<li v-for="(item, index) in items" :key="index">
				{{ item }}
			</li>
		</ul>

		<!-- Задание 2: Добавление в начало массива -->
		<input v-model="newItem" />
		<button @click="addItemToStart">Add to Start</button>

		<ul>
			<li v-for="(item, index) in items" :key="index">
				{{ item }}
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	data() {
		return {
			newItem: '',
			items: ['a', 'b', 'c', 'd', 'e'],
		};
	},
	methods: {
		addItem() {
			this.items.push(this.newItem);
			this.newItem = ''; // Очистка инпута после добавления
		},
		addItemToStart() {
			this.items.unshift(this.newItem);
			this.newItem = ''; // Очистка инпута после добавления
		}
	}
};
</script>
