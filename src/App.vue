<template>
	<div>
		<Employee @action1="handleAction1" @action2="handleAction2" />
	</div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
	components: {
		Employee,
	},
	methods: {
		handleAction1() {
			alert('Action 1 triggered!');
		},
		handleAction2() {
			alert('Action 2 triggered!');
		},
	},
};
</script>