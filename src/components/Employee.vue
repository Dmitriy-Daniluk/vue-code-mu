<template>
	<div>
		<button @click="triggerAction1">Action 1</button>
		<button @click="triggerAction2">Action 2</button>
	</div>
</template>

<script>
export default {
	emits: ['action1', 'action2'],
	methods: {
		triggerAction1() {
			this.$emit('action1');
		},
		triggerAction2() {
			this.$emit('action2');
		},
	},
};
</script>