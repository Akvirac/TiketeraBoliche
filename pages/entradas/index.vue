<script setup>
//Declaracion de variables.
var hNum = 0
var mNum = 0
var bNum = 0
var vTicket = 0

const totalNoche = ref([])
//Funciones

//Bandera para Numero de tickets.
console.log(vTicket)
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
		<div class="flex justify-center pt-16">
			<div>
				<Boton class="bg-blue-700 hover:bg-blue-900" @click="valorTicket"
					>Hombre</Boton
				>
				<div class="flex justify-center pt-2">
					<BotonS @click="vTicket = 2" class="hover:bg-blue-900">2</BotonS>
					<BotonS @click="valorTicket3" class="hover:bg-blue-900">3</BotonS>
					<BotonS @click="valorTicket4" class="hover:bg-blue-900">4</BotonS>
					<BotonS @click="valorTicket5" class="hover:bg-blue-900">5</BotonS>
				</div>
			</div>
			<div>
				<Boton class="bg-purple-700 hover:bg-purple-900" @click="ticketMujer"
					>Mujer</Boton
				>
				<div class="flex justify-center pt-2">
					<BotonS class="bg-purple-700 hover:bg-purple-900">2</BotonS>
					<BotonS class="bg-purple-700 hover:bg-purple-900">3</BotonS>
					<BotonS class="bg-purple-700 hover:bg-purple-900">4</BotonS>
					<BotonS class="bg-purple-700 hover:bg-purple-900">5</BotonS>
				</div>
			</div>
			<div>
				<Boton class="bg-teal-700 hover:bg-teal-900" @click="ticketBinario"
					>No Binario</Boton
				>
				<div class="flex justify-center pt-2">
					<BotonS class="bg-teal-700 hover:bg-teal-900">2</BotonS>
					<BotonS class="bg-teal-700 hover:bg-teal-900">3</BotonS>
					<BotonS class="bg-teal-700 hover:bg-teal-900">4</BotonS>
					<BotonS class="bg-teal-700 hover:bg-teal-900">5</BotonS>
				</div>
			</div>
		</div>
	</div>
	<div class="flex justify-center pt-32">
		<Boton class="bg-red-700" @click="cerrarCaja">Cerrar caja</Boton>
	</div>
</template>
