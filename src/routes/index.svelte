<script>
	import OneRowGrid from '$lib/ImageGrids/OneRowGrid.svelte';

	const photos = [
		'/images/women/woman1.jpg',
		'/images/women/woman2.jpg',
		'/images/women/woman3.jpg',
		'/images/women/woman4.jpg'
	];
</script>

<div class="section">
	<div class="max-width">
		<h1>Hello</h1>
		<div class="photo-box">
			<img src="/images/women/woman5.jpg" alt="wom1" />
			<OneRowGrid {photos} />
		</div>
	</div>
</div>

<style lang="scss">
	.photo-box {
		width: 100%;
		height: 65rem;

		img {
			width: 100%;
			height: 100%;
			object-fit: cover;
		}
	}
</style>
