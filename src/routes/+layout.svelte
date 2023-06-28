<script>
	import Header from './Menu.svelte';
	import './styles.css';
	import Footer from '../blocks/Footer.svelte';
</script>

<div class="app">
	<!-- <Header /> -->

	<main>
		<slot />
	</main>

	<Footer />
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
		/* width: 100%; */
		margin: 0 auto;
	}



	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	} 
</style>
