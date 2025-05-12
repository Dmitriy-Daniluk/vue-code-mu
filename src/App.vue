<template>
	<div id="app">
		<User :items="items" />
	</div>
</template>

<script>
import User from './components/Employee.vue';

export default {
	name: 'App',
	components: {
		User
	},
	data() {
		return {
			items: ['Apple', 'Banana', 'Orange', 'Grapes']
		};
	}
};
</script>

<style>
#app {
	text-align: center;
}
</style>
