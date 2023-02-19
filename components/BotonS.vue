<script setup>
defineProps({
	type: {
		type: String,
		default: 'button',
	},
})
</script>

<template>
	<button
		class="text-white bg-blue-700 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2"
		:type="type"
	>
		<slot />
	</button>
</template>
