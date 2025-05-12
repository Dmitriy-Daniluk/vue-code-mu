<template>
	<div>
		<p>{{ arr1[0] }}</p>
		<p>{{ arr1[1] }}</p>
		<p>{{ arr1[2] }}</p>

		<p>Сумма: {{ arr2[0] + arr2[1] + arr2[2] }}</p>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			arr1: ['x', 'y', 'z'],
			arr2: [1, 2, 3]
		};
	}
}
</script>
