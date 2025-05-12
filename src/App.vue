<template>
	<ul>
		<li v-for="(item, index) in items" :key="index" @click="removeItem(index)">
			{{ item }}
		</li>
	</ul>
</template>

<script>
export default {
	data() {
		return {
			items: ['a', 'b', 'c', 'd', 'e'],
		};
	},
	methods: {
		removeItem(index) {
			this.items.splice(index, 1);
		}
	}
};
</script>
