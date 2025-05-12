<template>
	<button @click="toggleVisibility">Скрыть абзацы</button>
	<template v-if="isVisible">
		<p>Абзац 1</p>
		<p>Абзац 2</p>
		<p>Абзац 3</p>
	</template>
</template>

<script>
export default {
	data() {
		return {
			isVisible: true
		}
	},
	methods: {
		toggleVisibility() {
			this.isVisible = !this.isVisible;
		}
	}
}
</script>
