<template>
	<div>
		<button @click="handleAction1">Action 1</button>
		<button @click="handleAction2">Action 2</button>
	</div>
</template>

<script>
export default {
	props: ['action1', 'action2'],
	methods: {
		handleAction1() {
			this.$emit('action1');
		},
		handleAction2() {
			this.$emit('action2');
		},
	},
};
</script>