<template>
	<div>
		<!-- Текст с применением CSS классов -->
		<p :class="obj">text</p>

		<!-- Кнопки для изменения видимости элемента -->
		<button @click="showElement">Show</button>
		<button @click="hideElement">Hide</button>
		<button @click="toggleElement">Toggle</button>
	</div>
</template>

<script>
export default {
	data() {
		return {
			obj: {
				hidden: true,
			},
		};
	},
	methods: {
		// Показывает элемент
		showElement() {
			this.obj.hidden = false;
		},
		// Скрывает элемент
		hideElement() {
			this.obj.hidden = true;
		},
		// Тогглит видимость элемента
		toggleElement() {
			this.obj.hidden = !this.obj.hidden;
		},
	},
};
</script>

<style>
/* Стили для скрытия текста */
p.hidden {
	display: none;
}
</style>
