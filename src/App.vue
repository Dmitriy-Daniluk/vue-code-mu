<template>
	<div>
		<!-- Checkbox с привязкой к свойству checked -->
		<input type="checkbox" v-model="checked">

		<!-- Абзац, который будет показан или скрыт в зависимости от состояния checkbox -->
		<p v-if="checked">Этот абзац отображается, если checkbox отмечен.</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			checked: false, // Изначально checkbox не отмечен
		};
	},
};
</script>
