<template>
	<div>
		<!-- Задание 1: Добавление нового элемента в конец списка -->
		<ul>
			<li v-for="elem in arr" :key="elem">{{ elem }}</li>
		</ul>
		<button @click="add">Add</button>

		<!-- Задание 2: Удаление первого элемента из списка -->
		<ul>
			<li v-for="elem in arr2" :key="elem">{{ elem }}</li>
		</ul>
		<button @click="removeFirst">Remove First</button>

		<!-- Задание 3: Удаление последнего элемента из списка -->
		<ul>
			<li v-for="elem in arr3" :key="elem">{{ elem }}</li>
		</ul>
		<button @click="removeLast">Remove Last</button>

		<!-- Задание 4: Удаление предпоследнего элемента из списка -->
		<ul>
			<li v-for="elem in arr4" :key="elem">{{ elem }}</li>
		</ul>
		<button @click="removeSecondLast">Remove Second Last</button>

		<!-- Задание 5: Сортировка элементов массива -->
		<ul>
			<li v-for="elem in arr5" :key="elem">{{ elem }}</li>
		</ul>
		<button @click="sortArray">Sort</button>

		<!-- Задание 6: Перевернуть порядок элементов массива -->
		<ul>
			<li v-for="elem in arr6" :key="elem">{{ elem }}</li>
		</ul>
		<button @click="reverseArray">Reverse</button>
	</div>
</template>

<script>
export default {
	data() {
		return {
			arr: ['a', 'b', 'c'], // Задание 1
			arr2: ['a', 'b', 'c'], // Задание 2
			arr3: ['a', 'b', 'c'], // Задание 3
			arr4: ['a', 'b', 'c'], // Задание 4
			arr5: ['c', 'b', 'a'], // Задание 5
			arr6: ['a', 'b', 'c'], // Задание 6
		};
	},
	methods: {
		// Задание 1: Добавление нового элемента в конец списка
		add() {
			this.arr.push('xxx');
		},
		// Задание 2: Удаление первого элемента из списка
		removeFirst() {
			this.arr2.shift();
		},
		// Задание 3: Удаление последнего элемента из списка
		removeLast() {
			this.arr3.pop();
		},
		// Задание 4: Удаление предпоследнего элемента из списка
		removeSecondLast() {
			if (this.arr4.length > 1) {
				this.arr4.splice(this.arr4.length - 2, 1);
			}
		},
		// Задание 5: Сортировка элементов массива
		sortArray() {
			this.arr5.sort();
		},
		// Задание 6: Перевернуть порядок элементов массива
		reverseArray() {
			this.arr6.reverse();
		},
	},
};
</script>
