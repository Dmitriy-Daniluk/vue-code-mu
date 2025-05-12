<template>
	<p v-if="visible">Первый абзац (visible = true)</p>

	<p v-if="!visible">Второй абзац (visible = false)</p>
</template>

<script>
export default {
	data() {
		return {
			visible: true,
		};
	}
}
</script>
