<script setup>
//Declaracion de variables.

//Bandera tipo entrada
let tipoEntrada = 0
//Bandera para Numero de tickets.
let cantidadTicket = 0
let hNum = 0
let mNum = 0
let bNum = 0

const totalNoche = ref([])
//Funciones

//imprimir ticket
function imprimirTicket() {
	if (tipoEntrada == 1) hNum = hNum + cantidadTicket
	if (tipoEntrada == 2) mNum = mNum + cantidadTicket
	if (tipoEntrada == 3) bNum = bNum + cantidadTicket

	console.log(hNum)
	console.log(mNum)
	console.log(bNum)
}
//Cerrar Caja
function cerrarCaja() {
	totalNoche.hombres = hNum
	totalNoche.mujeres = mNum
	totalNoche.binario = bNum
	totalNoche.total = hNum + mNum + bNum
	hNum = 0
	mNum = 0
	bNum = 0
	console.log(totalNoche.hombres)
	console.log(totalNoche.mujeres)
	console.log(totalNoche.binario)
	console.log(totalNoche.total)
}
</script>

<template>
	<div>
		<div class="flex justify-center pt-16 pb-16">
			<div>
				<Boton class="bg-blue-700 hover:bg-blue-900" @click="tipoEntrada = 1"
					>Hombres</Boton
				>
			</div>
			<div>
				<Boton
					class="bg-purple-700 active:bg-purple-900"
					@click="tipoEntrada = 2"
					>Mujeres</Boton
				>
			</div>
			<div>
				<Boton class="bg-teal-700 hover:bg-teal-900" @click="tipoEntrada = 3"
					>N. Binario</Boton
				>
			</div>
		</div>
		<div class="flex justify-center pt-2">
			<Boton
				size="small"
				class="bg-stone-800 hover:bg-violet-900"
				@click="cantidadTicket = 1"
				>1</Boton
			>
			<Boton
				size="small"
				class="bg-stone-800 hover:bg-violet-900"
				@click="cantidadTicket = 2"
				>2</Boton
			>
			<Boton
				size="small"
				class="bg-stone-800 hover:bg-violet-900"
				@click="cantidadTicket = 3"
				>3</Boton
			>
			<Boton
				size="small"
				class="bg-stone-800 hover:bg-violet-900"
				@click="cantidadTicket = 4"
				>4</Boton
			>
			<Boton
				size="small"
				class="bg-stone-800 hover:bg-violet-900"
				@click="cantidadTicket = 5"
				>5</Boton
			>
		</div>
	</div>
	<div>
		<div class="flex justify-center pt-32">
			<Boton class="bg-red-700 mb-2" @click="imprimirTicket">Imprimir</Boton>
		</div>
	</div>
</template>
