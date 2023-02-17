<script setup>
//Declaracion de variables.
var hNum = 0
var mNum = 0
var bNum = 0

const totalNoche = ref([])
//Funciones
//Contador hombres
function ticketHombre() {
	hNum = hNum + 1
	console.log(hNum)
}
//Contador mujeres
function ticketMujer() {
	mNum = mNum + 1
	console.log(mNum)
}
//Contador Binario
function ticketBinario() {
	bNum = bNum + 1
	console.log(bNum)
}
//Cerrar Caja
function cerrarCaja() {
	totalNoche.hombres = hNum
	totalNoche.mujeres = mNum
	totalNoche.binario = bNum
	totalNoche.total = hNum + mNum + bNum
	console.log(totalNoche.hombres)
	console.log(totalNoche.mujeres)
	console.log(totalNoche.binario)
	console.log(totalNoche.total)
}
</script>

<template>
	<div>
		<div class="grid grid-col-3">
			<div class="flex">
				<Boton class="bg-blue-700" @click="ticketHombre">Hombre</Boton>
			</div>
			<div>
				<Boton class="bg-purple-700" @click="ticketMujer">Mujer</Boton>
			</div>
			<div>
				<Boton class="bg-teal-700" @click="ticketBinario">No Binario</Boton>
			</div>
		</div>
	</div>
	<div>
		<Boton class="bg-yellow-700" @click="cerrarCaja">Cerrar caja</Boton>
	</div>
</template>
