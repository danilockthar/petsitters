<script>
	import { slide } from "svelte/transition";
</script>

<main>
	<div transition:slide>
		<p class="title-presentation">
			Tu mascota es parte de la familia,<span>
				cuídala con nosotros</span
			>.
		</p>
	</div>
	<img src="/doogy.svg" alt="presentation" />
</main>

<style>
	main {
		margin: 0 14vw;
		min-height: 90vh;
		display: grid;
		grid-template-columns: 1fr 1fr;
		align-items: center;
	}
	main img {
		width: 35vw;
		justify-self: end;
        animation: fade-in-rigth 1s ease-in-out forwards;
		animation-delay: 0.5s;
		opacity: 0;
		transform: translateX(10%);
	}
	.title-presentation {
		font-size: 4vw;
		color: white;
		font-weight: bold;
		line-height: 1;
		animation: fade-in-left 1s ease-in-out forwards;
		animation-delay: 0.5s;
		opacity: 0;
		transform: translateX(-10%);
	}
	.title-presentation span {
		color: #ffc727;
	}
    @keyframes fade-in-rigth {
		0% {
			opacity: 0;
			transform: translateX(10%);
		}
		100% {
			opacity: 1;
			transform: translateX(0%);
		}
	}
	@keyframes fade-in-left {
		0% {
			opacity: 0;
			transform: translateX(-10%);
		}
		100% {
			opacity: 1;
			transform: translateX(0%);
		}
	}
	/* @keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@-moz-keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@-webkit-keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@-o-keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@-ms-keyframes fadeIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
} */
</style>
