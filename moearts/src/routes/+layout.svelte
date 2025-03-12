<script>
	import Header from './Header.svelte';
	import '../app.css';

	/** @type {{children: import('svelte').Snippet}} */
	let { children } = $props();
</script>

<div class="app">
	<Header />

	<main>
		{@render children()}
	</main>

	<footer>
		
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		margin: 0 auto;
		padding: 0 16px;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}
	@media (max-width: 1100px) {
       
}

    @media (max-width: 1010px) {
		
       
}

    @media (max-width: 650px) {
		
  }
    @media (max-width: 375px) {
		
  }
	@media (min-width: 480px) {

	}
</style>
