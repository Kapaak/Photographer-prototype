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

<style global>
	*,
	*::before,
	*::after {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	html {
		font-size: 62.5%;
	}

	body {
		font-size: 1.6rem;
		font-family: 'Poppins', sans-serif;
	}

	:root {
		--col1: rgb(24, 24, 24);
		--col2: rgb(228, 228, 228);
	}

	.section {
		height: 100vh;
		min-height: 100vh;
	}

	.max-width {
		max-width: 130rem;
		margin: 0 auto;
		width: 100%;
		height: 100%;
	}

	.headline {
		font-size: 5rem;
	}

	.text {
		font-size: 1.8rem;
		line-height: 2;
	}
</style>
