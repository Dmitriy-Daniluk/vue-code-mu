<template>
	<div>
		<!-- Группа radio для выбора родного языка -->
		<input name="language" type="radio" v-model="nativeLanguage" value="English"> English
		<input name="language" type="radio" v-model="nativeLanguage" value="Spanish"> Spanish
		<input name="language" type="radio" v-model="nativeLanguage" value="French"> French

		<!-- Вывод выбранного языка -->
		<p>You have chosen: {{ nativeLanguage }}</p>

		<!-- В зависимости от выбора выводим текст на соответствующем языке -->
		<p v-if="nativeLanguage === 'English'">Hello, how are you?</p>
		<p v-if="nativeLanguage === 'Spanish'">Hola, ¿cómo estás?</p>
		<p v-if="nativeLanguage === 'French'">Bonjour, comment ça va?</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			// Переменная для хранения выбранного языка
			nativeLanguage: '',
		};
	},
};
</script>
