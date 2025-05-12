<template>
	<!-- Ссылка с обработчиком события и модификатором prevent -->
	<a href="https://yandex.ru" @click.prevent="handleLinkClick">Click me</a>

	<!-- Кнопка с обработчиком события, срабатывающего только один раз -->
	<button @click.once="handleButtonClick">Click me once</button>
</template>

<script>
export default {
	methods: {
		// Обработчик клика по ссылке
		handleLinkClick() {
			alert('Ссылка была нажата, но переход не произошел!');
		},

		// Обработчик клика по кнопке
		handleButtonClick() {
			alert('Вы кликнули по кнопке первый раз!');
		}
	}
}
</script>
