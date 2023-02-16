<script setup></script>

<template>
	<div>
		<div class="border-b-2 border-emerald-500 text-xl font-semibold">
			<header class="shadow-sm bg-white">
				<nav class="p-2 flex justify-between">
					<ul class="flex gap-4">
						<li><NuxtLink to="/entradas"> Entradas </NuxtLink></li>
					</ul>
					<ul>
						<li><NuxtLink to="./"> Volver </NuxtLink></li>
					</ul>
				</nav>
			</header>
		</div>
		<div>
			<slot />
		</div>
	</div>
</template>
