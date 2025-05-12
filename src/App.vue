<template>
	<div>
		<!-- Задача 1: Квадратный корень -->
		<p>{{ res }}</p>
		<input v-model="num">
		<button @click="calcSquareRoot">Get Square Root</button>

		<!-- Задача 2: Сумма двух чисел -->
		<p>{{ sum }}</p>
		<input v-model.number="num1" type="number">
		<input v-model.number="num2" type="number">
		<button @click="calcSum">Calculate Sum</button>

		<!-- Задача 3: Переключение текста между инпутами -->
		<p>{{ text1 }} - {{ text2 }}</p>
		<input v-model="text1">
		<input v-model="text2">
		<button @click="swapText">Swap Text</button>

		<!-- Задача 4: Разделение ФИО -->
		<p>{{ lastName }}</p>
		<p>{{ firstName }}</p>
		<p>{{ patronymic }}</p>
		<input v-model="fullName" placeholder="Enter full name">
		<button @click="splitName">Split Name</button>
	</div>
</template>

<script>
export default {
	data() {
		return {
			num: 0,
			res: 0,
			num1: 0,
			num2: 0,
			sum: 0,
			text1: '',
			text2: '',
			fullName: '',
			lastName: '',
			firstName: '',
			patronymic: ''
		};
	},
	methods: {
		// Задача 1: Получение квадратного корня
		calcSquareRoot() {
			this.res = Math.sqrt(this.num);
		},

		// Задача 2: Сумма двух чисел
		calcSum() {
			this.sum = this.num1 + this.num2;
		},

		// Задача 3: Переключение текста
		swapText() {
			const temp = this.text1;
			this.text1 = this.text2;
			this.text2 = temp;
		},

		// Задача 4: Разделение ФИО
		splitName() {
			const nameParts = this.fullName.split(' ');
			if (nameParts.length === 3) {
				this.lastName = nameParts[0];
				this.firstName = nameParts[1];
				this.patronymic = nameParts[2];
			} else {
				this.lastName = this.firstName = this.patronymic = '';
			}
		}
	}
};
</script>
