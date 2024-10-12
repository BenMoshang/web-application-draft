<script>
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	import '../app.css';
	import '../lib/global/global.classes.css';
	import '../lib/global/utils.css';
</script>

<section class="layout">
	<Header />

	<main class="layout__main">
		<slot />

		<h1 class="text-red-500">layout</h1>
	</main>

	<Footer />
</section>

<style>
	.layout{
		display: flex;
		flex-direction: column;
		min-height: 100dvh;

		& .layout__main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		max-width: var(--max-width);
		margin: 0 auto;
		box-sizing: border-box;
		padding-inline: .5rem;


	}
	}


	

</style>
