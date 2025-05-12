<template>
	<ul>
		<li v-for="(item, index) in items" :key="index">
			{{ item }}
		</li>
	</ul>
</template>

<script>
export default {
	props: ['items']
};
</script>

<style scoped>
ul {
	list-style-type: none;
	padding: 0;
}

li {
	margin: 5px 0;
}
</style>
