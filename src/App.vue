<template>
	<div>
		<!-- Тег с инлайн объектом с классами -->
		<p :class="{ active: true, valid: false }">text</p>
	</div>
</template>

<script>
export default {
	data() {
		return {};
	}
};
</script>

<style>
/* Стили для классов */
.active {
	color: green;
}

.valid {
	color: red;
}
</style>
