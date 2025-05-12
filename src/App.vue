<template>
	<div>
		<!-- Кнопка для вызова метода -->
		<button @click="showDate">Показать текущую дату</button>
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
