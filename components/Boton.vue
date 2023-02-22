<script setup>
defineProps({
	type: {
		type: String,
		default: 'button',
	},
	size: {
		type: String,
		default: 'regular',
	},
})
</script>

<template>
	<button
		:class="[[size == 'small' && 'p-8']]"
		class="w-fit text-white text-2xl focus:ring-4 rounded-lg text-center inline-flex items-center mr-2 p-12"
		:type="type"
	>
		<slot />
	</button>
</template>
