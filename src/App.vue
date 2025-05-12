<template>
	<div>
		<!-- Элемент с динамически добавляемыми классами -->
		<p :class="{ valid: isValid, disabled: isDisabled }">
			text
		</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			isValid: true,
			isDisabled: true,
		};
	}
};
</script>

<style>
/* Стили для классов */
.valid {
	color: green;
}

.disabled {
	color: gray;
	text-decoration: line-through;
}
</style>
