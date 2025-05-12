<template>
	<div>
		<!-- Задание 1 -->
		<h2>Задание 1: Показать абзац</h2>
		<button @click="show">show</button>
		<p v-if="visible">text</p>

		<!-- Задание 2 -->
		<h2>Задание 2: Показать и скрыть абзац</h2>
		<button @click="show">show</button>
		<button @click="hide">hide</button>
		<p v-if="visible">text</p>

		<!-- Задание 3 -->
		<h2>Задание 3: Показать только одну кнопку в зависимости от состояния</h2>
		<button v-if="!visible" @click="show">show</button>
		<button v-if="visible" @click="hide">hide</button>
		<p v-if="visible">text</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			visible: false,
		}
	},
	methods: {
		show() {
			this.visible = true;
		},
		hide() {
			this.visible = false;
		}
	}
}
</script>
