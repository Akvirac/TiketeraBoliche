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
		class="text-white text-4xl bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full p-12 text-sm p-2.5 text-center inline-flex items-center mr-2 p-8"
		:type="type"
	>
		<slot />
	</button>
</template>
