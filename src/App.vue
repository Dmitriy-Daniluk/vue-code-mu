<template>
	<div>
		<!-- Абзац 1 -->
		<button @click="toggle(1)">
			{{ visible1 ? 'hide' : 'show' }}
		</button>
		<p v-if="visible1">text 1</p>

		<!-- Абзац 2 -->
		<button @click="toggle(2)">
			{{ visible2 ? 'hide' : 'show' }}
		</button>
		<p v-if="visible2">text 2</p>

		<!-- Абзац 3 -->
		<button @click="toggle(3)">
			{{ visible3 ? 'hide' : 'show' }}
		</button>
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
