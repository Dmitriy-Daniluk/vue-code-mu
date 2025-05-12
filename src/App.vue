<template>
	<div>
		<!-- Кнопка для вывода текущей даты по клику -->
		<button @click="showDate">Показать текущую дату (клик)</button>

		<!-- Кнопка для вывода текущей даты по наведению мыши -->
		<button @mouseover="showDate">Показать текущую дату (наведение)</button>
	</div>
</template>

<script>
export default {
	name: 'App',
	methods: {
		showDate() {
			// Получаем текущую дату и показываем её в alert
			alert(new Date().toLocaleString());
		}
	}
}
</script>
