<template>
	<div>
		<!-- Выпадающий список для выбора города -->
		<select v-model="selectedCity">
			<option>New York</option>
			<option>Los Angeles</option>
			<option>Chicago</option>
			<option>San Francisco</option>
		</select>

		<!-- Вывод выбранного города -->
		<p>You live in: {{ selectedCity }}</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			// Переменная для хранения выбранного города
			selectedCity: 'New York', // Значение по умолчанию
		};
	},
};
</script>
