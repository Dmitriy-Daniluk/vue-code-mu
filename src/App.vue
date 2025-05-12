<template>
	<div>
		<!-- Задание 1 -->
		<input v-model="text" @keyup.enter="showText" />
		<p>{{ text }}</p>

		<!-- Задание 2 -->
		<a href="#" @click.ctrl="showCtrlText">Click me</a>
		<p>{{ ctrlText }}</p>

		<!-- Задание 3 -->
		<a href="#" @mousedown.left="showLeftClick" @mousedown.right="showRightClick"
			@mousedown.middle="showMiddleClick">Click me with mouse buttons</a>
		<p>{{ mouseText }}</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			text: '',
			ctrlText: '',
			mouseText: ''
		};
	},
	methods: {
		showText() {
			this.ctrlText = this.text;
		},
		showCtrlText() {
			this.ctrlText = 'Ctrl key was pressed!';
		},
		showLeftClick() {
			this.mouseText = 'left';
		},
		showRightClick() {
			this.mouseText = 'right';
		},
		showMiddleClick() {
			this.mouseText = 'middle';
		}
	}
};
</script>
