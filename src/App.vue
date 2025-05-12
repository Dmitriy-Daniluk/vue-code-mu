<template>
	<p v-if="isAdmin">Admin</p>
	<p v-else>User</p>
</template>

<script>
export default {
	data() {
		return {
			isAdmin: true, // или false
		}
	}
}
</script>
