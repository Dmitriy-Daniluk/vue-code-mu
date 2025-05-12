<template>
	<div>
		<!-- Задача 1: Текст из инпута сразу выводится в абзаце -->
		<input v-model="message">
		<p>{{ message }}</p>

		<!-- Задача 2: Текст выводится в верхнем регистре -->
		<input v-model="message">
		<p>{{ message.toUpperCase() }}</p>

		<!-- Задача 3: Квадрат введенного числа -->
		<input v-model.number="number" type="number">
		<p>{{ number * number }}</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			message: '',
			number: 0,
		};
	},
};
</script>
