<template>
	<div>
		<p>Name: {{ name }}</p>
		<p>Salary: {{ salary }}</p>
		<p>Age: {{ age }}</p>
	</div>
</template>

<script>
export default {
	props: ['name', 'salary', 'age']
}
</script>
