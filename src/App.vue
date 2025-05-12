<template>
	<p v-if="age < 18">Подросток</p>
	<p v-else-if="age >= 19 && age <= 25">Молодой человек</p>
	<p v-else>Мужчина</p>
</template>

<script>
export default {
	data() {
		return {
			age: 25,
		}
	}
}
</script>
