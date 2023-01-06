<script>
	// let mm = gsap.matchMedia();
	export let name;
	import { onMount } from "svelte";
	import { gsap } from "gsap/dist/gsap";
	onMount(() => {
		gsap.to(".background", 2.4, {
			y: "-100%",
			ease: "Expo.easeInOut",
			delay: 0,
		});
	});

</script>

<section>
	<div class="background" />
	<img class="statue" src="/assets/img1.jpg" alt="statue" />
	<h2 class="title">{name} </h2>
</section>

<style>
	h2 {
		position: absolute;
		text-align: center;
		font-size: 3.5em;
		font-family: "NewYork";
		font-weight: bolder;
		color: #2584ec;
	}
	section {
		padding: 1em 1em;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}
	.background {
		background: #bebeb8;
		opacity: 1;
		position: absolute;
		top: 0;
		bottom: 0;
		right: 0;
		left: 0;
		z-index: 2;
	}

	img {
	    width: 100%;
		height: 80vh;
		object-fit: cover;
	}

	@media (min-width: 70rem) {
		section {
			padding: 0;
		}

		h2 {
			font-size: 1em;
			font-weight: 200;
		}
		img {
			max-width: 35%;
			max-height:75vh;
		}
	}

	@media (min-width: 45rem) {

		h2 {
			font-size: 9em;
			font-weight: 500;
		}

	}
</style>
