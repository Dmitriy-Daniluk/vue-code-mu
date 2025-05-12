<template>
	<div>
		<!-- Выводим вычисляемое свойство price -->
		<p>Цена за один продукт: {{ cost }}</p>
		<p>Количество продуктов: {{ amount }}</p>
		<p>Полная стоимость: {{ price }}</p>

		<!-- Кнопка для изменения стоимости -->
		<button @click="increaseCost">Увеличить цену</button>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			cost: 100,  // Цена одного продукта
			amount: 5,  // Количество продуктов
		};
	},
	computed: {
		// Вычисляемое свойство для полной стоимости
		price() {
			return this.cost * this.amount;
		}
	},
	methods: {
		// Метод для изменения стоимости
		increaseCost() {
			this.cost += 10;  // Увеличиваем цену на 10
		}
	}
}
</script>
