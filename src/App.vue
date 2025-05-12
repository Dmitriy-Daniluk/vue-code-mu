<template>
	<div>
		<!-- Задача 1: Текст из textarea в абзаце -->
		<textarea v-model="text"></textarea>
		<p>{{ text }}</p>

		<!-- Задача 2: Разделение текста на слова и вывод в список -->
		<textarea v-model="textInput"></textarea>
		<button @click="generateWordList">Generate Word List</button>
		<ul>
			<li v-for="(word, index) in wordList" :key="index">{{ word }}</li>
		</ul>
	</div>
</template>

<script>
export default {
	data() {
		return {
			text: '',
			textInput: '',
			wordList: []
		};
	},
	methods: {
		// Задача 2: Получение массива слов из текста
		generateWordList() {
			// Разбиваем текст на массив слов
			this.wordList = this.textInput.split(/\s+/).filter(word => word.length > 0);
		}
	}
};
</script>
