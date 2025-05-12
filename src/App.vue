<template>
	<div>
		<!-- Выводим текст -->
		<p>{{ text }}</p>

		<!-- Кнопки для изменения значения свойства text -->
		<button @click="changeText('Первое значение')">Кнопка 1</button>
		<button @click="changeText('Второе значение')">Кнопка 2</button>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			text: 'Начальное значение',
		};
	},
	methods: {
		// Метод для изменения значения text
		changeText(newText) {
			this.text = newText;
		}
	}
}
</script>
