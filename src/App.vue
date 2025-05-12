<template>
	<div>
		<!-- Селект для выбора дня недели -->
		<select v-model="selectedDay">
			<option v-for="day in days" :key="day">{{ day }}</option>
		</select>
		<p>Selected Day: {{ selectedDay }}</p>

		<!-- Селект для выбора дня, месяца и года -->
		<div>
			<select v-model="selectedDayOfMonth">
				<option v-for="day in daysOfMonth" :key="day">{{ day }}</option>
			</select>
			<select v-model="selectedMonth">
				<option v-for="month in months" :key="month">{{ month }}</option>
			</select>
			<select v-model="selectedYear">
				<option v-for="year in years" :key="year">{{ year }}</option>
			</select>

			<p>Selected Date: {{ selectedDayOfMonth }} {{ selectedMonth }} {{ selectedYear }}</p>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			// Список дней недели
			days: ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'],
			selectedDay: '', // Выбранный день недели

			// Списки для дня, месяца и года
			daysOfMonth: Array.from({ length: 31 }, (_, i) => i + 1),
			months: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
			years: Array.from({ length: 100 }, (_, i) => 2025 - i), // Последние 100 лет
			selectedDayOfMonth: '', // Выбранный день месяца
			selectedMonth: '', // Выбранный месяц
			selectedYear: '', // Выбранный год
		};
	},
	created() {
		// Устанавливаем текущие дату по умолчанию
		const currentDate = new Date();
		this.selectedDayOfMonth = currentDate.getDate();
		this.selectedMonth = this.months[currentDate.getMonth()];
		this.selectedYear = currentDate.getFullYear();
		this.selectedDay = this.days[currentDate.getDay()];
	},
};
</script>
