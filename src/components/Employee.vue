<template>
	<div>
		<h2>Employee: {{ name }}</h2>
		<p>Position: {{ position }}</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			name: 'john',
			position: 'Developer'
		};
	}
};
</script>

<style scoped>
h2 {
	color: blue;
}
</style>
