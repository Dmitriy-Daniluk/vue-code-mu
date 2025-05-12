<!-- components/Employee.vue -->
<template>
	<div>
		<h2>Name: {{ name }}</h2>
		<h3>Surname: {{ surn }}</h3>
		<p>Age: {{ age }}</p>
	</div>
</template>

<script>
export default {
	props: ['name', 'surn', 'age']
};
</script>

<style scoped>
h2 {
	color: green;
}

h3 {
	color: blue;
}

p {
	color: gray;
}
</style>
