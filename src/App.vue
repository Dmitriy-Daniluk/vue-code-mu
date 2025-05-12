<template>
	<div>
		<!-- Кнопки с передачей параметров -->
		<button @click="showSquare(2)">Показать квадрат 2</button>
		<button @click="showSquare(3)">Показать квадрат 3</button>
	</div>
</template>

<script>
export default {
	name: 'App',
	methods: {
		// Метод принимает число и выводит его квадрат
		showSquare(num) {
			alert(num * num);
		}
	}
}
</script>
