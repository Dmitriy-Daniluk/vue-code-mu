<template>
	<div>
		<!-- Кнопка для показа текущего дня недели -->
		<button @click="showCurrentDay">Показать текущий день недели</button>

		<!-- Кнопка для показа дня недели по текущему числу -->
		<button @click="showDayFromNumber">Показать день недели по числу</button>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			// Получаем текущий день недели (0 - воскресенье, 6 - суббота)
			dayNumber: new Date().getDay(),
			// Можно задать любое число для теста (например, 2 - вторник)
			testNumber: 2
		};
	},
	methods: {
		// Вспомогательный метод для получения дня недели по числу
		getDayByNumber(number) {
			const days = ['Воскресенье', 'Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота'];
			return days[number];
		},
		// Основной метод для вывода текущего дня недели
		showCurrentDay() {
			const currentDay = this.getDayByNumber(this.dayNumber);
			alert(`Сегодня: ${currentDay}`);
		},
		// Основной метод для вывода дня недели по числу
		showDayFromNumber() {
			const day = this.getDayByNumber(this.testNumber);
			alert(`День недели для числа ${this.testNumber}: ${day}`);
		}
	}
}
</script>
