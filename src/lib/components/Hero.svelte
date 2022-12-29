<script>
    export let name;
</script>

<section>
    <img src="/assets/img1.jpg" alt="statue">
    <h2>{name} </h2>
</section>

<style>
    h2{
        position: absolute;
		background: none;
		font-size: 3.5em;
		font-family: "NewYork";
		font-weight: bolder;
		color: #2584ec;
    }
    	section {
            padding: 2em 1em;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}
	img {
		width: 100%;
		height: 70vh;
		object-fit: cover;
	}

	@media (min-width: 70rem) {
        img {
			width: 70%;
			height: 60vh;
		}
}
</style>
