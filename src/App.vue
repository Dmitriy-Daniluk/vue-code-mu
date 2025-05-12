<template>
	<div>
		<!-- Кнопка для блокировки и разблокировки инпута -->
		<input v-bind:disabled="isDisabled" type="text" />
		<button @click="toggleInput">Toggle Disabled</button>

		<!-- Чекбокс для регулирования состояния инпута -->
		<input type="checkbox" v-model="isDisabled"> Enable Input
	</div>
</template>

<script>
export default {
	data() {
		return {
			isDisabled: true, // Начальное состояние инпута заблокировано
		};
	},
	methods: {
		toggleInput() {
			this.isDisabled = !this.isDisabled;
		}
	}
};
</script>
