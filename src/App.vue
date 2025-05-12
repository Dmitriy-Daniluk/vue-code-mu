<template>
	<ul>
		<li v-for="(value, key, index) in obj" :key="key">
			{{ key }} - {{ value }} - {{ index + 1 }}
		</li>
	</ul>
</template>

<script>
export default {
	data() {
		return {
			obj: {
				user1: '100$',
				user2: '200$',
				user3: '300$',
			},
		};
	},
};
</script>
