<script lang="ts">
	import '../style/index.scss';
	import favicon from '$lib/assets/favicon.svg';
	import Menu from '../components/Menu.svelte';
	import Footer from '../components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<title>Unitá Estética e Saúde Integrativa</title>
	<link rel="icon" href={favicon} />
</svelte:head>

<div id="root">
	<header>
		<Menu />
	</header>

	<main>
		{@render children?.()}
	</main>

	<Footer />
</div>

<style lang="scss">
	header {
		align-items: center;
		display: flex;
		backdrop-filter: blur(10px);

		/* Remove os borders antigos */
		border: none;

		/* Border-top */
		border-top: 1px solid transparent;
		border-image: linear-gradient(
			to right,
			transparent,
			rgba(var(--secondary-rgb), 0.9),
			transparent
		) 1;

		/* Border-bottom */
		border-bottom: 1px solid transparent;
		border-image-slice: 1;
		border-image-source: linear-gradient(
			to right,
			transparent,
			rgba(var(--secondary-rgb), 1),
			transparent
		);

		height: 80px;
		margin: 8px 0 32px 0;
		position: sticky;
		top: 0;
		left: 0;
		z-index: 1000;
	}

	main {
		padding: 32px 16px;
	}
</style>

