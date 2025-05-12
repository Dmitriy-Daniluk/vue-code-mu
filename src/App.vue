<template>
	<div id="app">
		<Employee :name="employeeName" :surn="employeeSurn" :age="employeeAge" />
	</div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
	name: 'App',
	components: {
		Employee
	},
	data() {
		return {
			employeeName: 'Jogn',
			employeeSurn: 'Smit',
			employeeAge: 30
		};
	}
};
</script>

<style>
#app {
	text-align: center;
}
</style>
