<script>
	export let title;
	export let date;
	import { onMount } from "svelte";
	import { gsap } from "gsap/dist/gsap";
	onMount(() => {
        gsap.from(
        "header, footer ,h2 ",
        2,
        {
          y: "200",
          opacity: 0,
          ease: "Expo.easeInOut",
          delay: 2,
          stagger: 0.08,
        }
      );

      gsap.from("img",1, {
        scale: 1,
        ease: "Expo.easeOut",
        delay: 4,
		opacity: 1,
      });
	});
</script>

<header>
	<a href="/"><h1>{title}</h1></a>
	<p>{date}</p>
	<nav>
		<ul>
			<li>Projects</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		gap:3em;
	    padding: 2em 2em;
		font-family: "Monument Extended";
	}

	h1 {
		font-size: 1.2em;

		font-family: "Monument Extended";
	}
	p{
		font-size: 1.2em;
	}
	@media (min-width: 70rem) {
		header {
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: first baseline;
			padding: 3em 5em;
		}
		nav {
			font-size: 1.5em;
		}
		ul {
			display: flex;
			flex-direction: row;
			/* font-size: 1.2em; */
		}
		p {
			font-size: 1.5em;
		}
		h1 {
			font-size: 1.5em;
		}
	}
</style>
