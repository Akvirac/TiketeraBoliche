<script setup>
const totalNoche = ref({})

var hNum = 0

function ticketHombre() {
	hNum = hNum + 1
	totalNoche.hombres = hNum
	totalNoche.value.push(hNum)

	console.log(totalNoche)
}
</script>
<template>
	<div>
		<div>
			<Boton
				@click="ticketHombre"
				class="text-white text-2xl bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full p-12 text-sm p-2.5 text-center inline-flex items-center mr-2"
				>Hombre</Boton
			>
		</div>
		<div>
			<Boton
				@click="ticketMujer"
				class="text-white text-2xl bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full p-12 text-sm p-2.5 text-center inline-flex items-center mr-2"
				>Mujer</Boton
			>
		</div>
		<div>
			<Boton
				@click="ticketBinarie"
				class="text-white text-2xl bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full p-12 text-sm p-2.5 text-center inline-flex items-center mr-2"
				>No Binario</Boton
			>
		</div>
	</div>
</template>
