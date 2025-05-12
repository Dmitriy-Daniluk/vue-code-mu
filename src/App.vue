<template>
	<!-- №1 -->
	<div v-for="item in items" :key="item">{{ item }}</div>

	<!-- №2 -->
	<div v-for="item in items" :key="item">{{ item * item }}</div>

	<!-- №3 -->
	<ul>
		<li v-for="item in items" :key="item">{{ item }}</li>
	</ul>
</template>

<script>
export default {
	data() {
		return {
			items: [1, 2, 3, 4, 5],
		};
	},
};
</script>
