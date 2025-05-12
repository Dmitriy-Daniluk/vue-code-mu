<template>
	<a :href="href">{{ text }}</a>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			text: 'page',
			href: 'page.html'
		};
	}
}
</script>
