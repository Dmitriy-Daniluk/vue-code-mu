<template>
	<div>
		<!-- Вывод значений объекта -->
		<p>{{ obj.a }}</p>
		<p>{{ obj.b }}</p>
		<p>{{ obj.c }}</p>

		<!-- Сумма элементов объекта -->
		<p>Сумма: {{ obj.x + obj.y + obj.z }}</p>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			obj: { x: 1, y: 2, z: 3 }
		};
	}
}
</script>
