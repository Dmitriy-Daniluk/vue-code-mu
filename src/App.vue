<template>
	<div>
		<!-- Абзац 1 -->
		<button @click="toggle(1)">toggle 1</button>
		<p v-if="visible1">text 1</p>

		<!-- Абзац 2 -->
		<button @click="toggle(2)">toggle 2</button>
		<p v-if="visible2">text 2</p>

		<!-- Абзац 3 -->
		<button @click="toggle(3)">toggle 3</button>
		<p v-if="visible3">text 3</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			visible1: false,
			visible2: false,
			visible3: false,
		}
	},
	methods: {
		toggle(number) {
			this[`visible${number}`] = !this[`visible${number}`];
		}
	}
}
</script>
