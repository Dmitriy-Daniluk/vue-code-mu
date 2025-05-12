<template>
	<div>
		<!-- Группа checkbox для выбора языков -->
		<input type="checkbox" v-model="languages" value="English"> English
		<input type="checkbox" v-model="languages" value="Spanish"> Spanish
		<input type="checkbox" v-model="languages" value="French"> French
		<input type="checkbox" v-model="languages" value="German"> German
		<input type="checkbox" v-model="languages" value="Russian"> Russian

		<!-- Список языков, выбранных пользователем -->
		<ul>
			<li v-for="(language, index) in languages" :key="index">{{ language }}</li>
		</ul>
	</div>
</template>

<script>
export default {
	data() {
		return {
			// Массив для хранения выбранных языков
			languages: [],
		};
	},
};
</script>
