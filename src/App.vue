<template>
	<button @click="$emit('customEvent', 'parameter1', 'parameter2')">
		Нажми меня
	</button>
</template>
