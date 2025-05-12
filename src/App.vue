<template>
	<p :class="cssClasses">text</p>
</template>

<script>
export default {
	data() {
		return {
			cssClasses: 'active valid'
		}
	}
}
</script>
