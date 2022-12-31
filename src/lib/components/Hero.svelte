<script>
	let mm = gsap.matchMedia();
	export let name;
	import { onMount } from "svelte";
	import { gsap } from "gsap/dist/gsap";
	onMount(() => {
		gsap.to(".background", 2.4, {
			y: "-100%",
			ease: "Expo.easeInOut",
			delay: 0,
		});
		gsap.to("img", 4, {
			scale: "1",
			ease: "Expo.easeInOut",
			delay: 0,
		});

		gsap.to("img", 2.4, {
			width: "500",
			height: "700",
			padding: "none",
			ease: "Expo.easeInOut",
			delay: 3.2,
		});
		mm.add("(min-width: 2000px)", () => {
			gsap.to("img", 2.4, {
				width: "1000",
				height: "1800",
				padding: "none",
				ease: "Expo.easeInOut",
				delay: 3.2,
			});

			// this setup code only runs when viewport is at least 800px wide
		});
		gsap.from("img", 0.4, {
			opacity: 0,
			ease: "Expo.easeInOut",
			delay: 3.4,
		});
	});
</script>

<section>
	<div class="background" />
	<img src="/assets/img1.jpg" alt="statue" />
	<h2 class="title">{name} </h2>
</section>

<style>
	h2 {
		position: absolute;
		font-size: 3.5em;
		font-family: "NewYork";
		font-weight: bolder;
		color: #2584ec;
	}
	section {
		padding: 0.5em 1em;
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
		max-width: 100%;
		height: 70vh;
		object-fit: cover;
	}

	@media (min-width: 70rem) {
		section {
			padding: 0;
		}

		h2 {
			font-size: 12em;
			font-weight: 200;
		}
		img {
			width: 70%;
			height: 90vh;
		}
	}
</style>
