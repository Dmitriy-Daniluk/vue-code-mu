<template>
	<div>
		<template v-for="elem in items" :key="elem">
			<p>{{ elem }}</p>
			<p class="divider"></p>
		</template>
	</div>

	<ul>
		<template v-for="elem in items" :key="elem">
			<li>{{ elem }}</li>
			<li class="divider"></li>
		</template>
	</ul>
</template>

<script>
export default {
	data() {
		return {
			items: [1, 2, 3],
		};
	},
};
</script>
