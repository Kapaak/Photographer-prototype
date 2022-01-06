<script>
	import Navigation from '$lib/Navigation/index.svelte';
</script>

<svelte:head>
	<title>Photo | Walker</title>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<main>
	<Navigation />
	<slot />
</main>

<style global lang="scss">
	@use '../styles/hover-effect';
	@use '../styles/resets';
	@use '../styles/variables';
	@use '../styles/components';
	@use '../styles/layout';
</style>
