<template>
	<Employee :name="name" :salary="salary" :age="age" />
</template>

<script>
import Employee from './components/Employee.vue'

export default {
	components: {
		Employee
	},
	data() {
		return {
			name: 'John Doe',
			salary: 50000,
			age: 30
		}
	}
}
</script>
