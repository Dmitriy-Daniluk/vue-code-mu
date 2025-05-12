<template>
	<div>
		<button @click="show">Показать текст</button>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			text: 'str'
		};
	},
	methods: {
		show() {
			// Выводим значение свойства text
			alert(this.text);
		}
	}
}
</script>
