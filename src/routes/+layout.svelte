<script>
	import Header from "../lib/layout/Header.svelte";
	import Footer from "../lib/layout/Footer.svelte";
	import '../app.css';
	import '../lib/global-css/global.classes.css';
	import '../lib/global-css/utils.css';
</script>

<section class="layout">
	<Header />

	<main class="layout__main">
		<slot />
	</main>

	<Footer />
</section>

<style>
	.layout{
		display: flex;
		flex-direction: column;
		height: 100dvh;
		width: 100%;

		& .layout__main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		max-width: 120rem;
		margin: 0 auto;
		box-sizing: border-box;
		padding-inline: .5rem;
	}
	}


	

</style>
