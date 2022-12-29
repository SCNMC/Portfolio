<script>
    export let title;
    export let date;
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
    
    header{
	display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		gap: 1em;
		padding: 2em 1em;
		font-family: "Monument Extended";
    }


	h1 {
        font-size: 1.3em;
        margin: 0 auto;

		font-family: "Monument Extended";
	}


	@media (min-width: 70rem) {
		header {
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: first baseline;
			padding: 3em 5em;
		}
        nav{
            font-size: 1.2em;
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
