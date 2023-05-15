<script>
	import { onMount } from "svelte";
	const showlist = [
		"dani",
		"pepe",
		"juan",
		"roberto",
		"caro",
		"lucho",
		"theon",
	];

	let index = 0;
	let elementos = [];

	function mostrarSiguienteElemento() {
		// Oculta el elemento actual
		/* elementos[index].style.opacity = 0; */
		console.log({ index });
		console.log("INDEX", elementos[index]);
		index = (index + 1) % elementos.length;
		// Calcula el índice del siguiente elemento
		/* index = (index + 1) % elementos.length; */

		// Muestra el siguiente elemento
		/* elementos[index].style.opacity = 1; */
	}

	// Función que se ejecuta al montar el componente
	onMount(() => {
		// Obtiene todos los elementos del carrusel
		console.log(elementos);
		// Muestra el primer elemento

		// Repite la animación cada 10 segundos
		/* setInterval(mostrarSiguienteElemento, 1000); */
	});
</script>

<main>
	<div class=".contenedor">
		{#each showlist as item, i}
			<p class=".elemento" bind:this={elementos[i]}>{item}</p>
		{/each}
	</div>
</main>

<style>
	main {
		box-sizing: border-box;
		padding: 5vw;
		width: 100%;
		min-height: 50vh;
		display: grid;
	}
	div {
		justify-self: center;
		display: flex;
		overflow: hidden;
		flex-wrap: wrap;
		grid-auto-flow: column;
	}
	p {
		flex: 0 0 calc(33.33% - 10px); /* Establece el ancho de cada elemento */
		margin-right: 10px; /* Agrega un margen entre los elementos */
		margin-bottom: 10px; /* Agrega un margen inferior a los elementos */
		animation: slide-in 10s linear infinite;
	}
	p:nth-child(n + 4) {
		opacity: 0;
	}

	/* Anima los elementos */
	@keyframes slide-in {
		0% {
			margin-left: 0;
		}
		16.67% {
			margin-left: -33.33%;
		}
		33.33% {
			margin-left: -66.67%;
		}
		50% {
			margin-left: -100%;
		}
		66.67% {
			margin-left: -66.67%;
		}
		83.33% {
			margin-left: -33.33%;
		}
		100% {
			margin-left: 0;
		}
	}
</style>
