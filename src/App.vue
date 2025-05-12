<template>
	<div>
		<Employee v-for="user in users" :key="user.id" :name="user.name" :salary="user.salary" :age="user.age" />
	</div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
	components: {
		Employee,
	},
	data() {
		return {
			users: [
				{
					id: 1,
					name: 'name1',
					salary: 100,
					age: 30,
				},
				{
					id: 2,
					name: 'name2',
					salary: 200,
					age: 40,
				},
				{
					id: 3,
					name: 'name3',
					salary: 300,
					age: 50,
				},
			],
		};
	},
};
</script>
