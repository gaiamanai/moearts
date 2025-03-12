<script>
	import HeroSection from "./HeroSection.svelte";
</script>

<svelte:head>
	
	<title>GaiaMoe</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<HeroSection></HeroSection>
	
</section>

<style>
	/* Rende l'intera pagina full-width e responsive */
	* {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
		
	}

	html, body {
		width: 100%;
		height: 100%;
		background-color: #0D0D0D; /* Cambia il colore di sfondo in nero */
		color: #F5F5F5;
	}


	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: auto;
	}
</style>
