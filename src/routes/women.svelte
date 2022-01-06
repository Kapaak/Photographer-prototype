<script>
	import ThreePicGrid from '$lib/ImageGrids/ThreePicGrid.svelte';

	const photos = [
		'/images/women/woman1.jpg',
		'/images/women/woman2.jpg',
		'/images/women/woman3.jpg'
	];
</script>

<div class="section">
	<div class="max-width">
		<div class="photo-container">
			<ThreePicGrid {photos} />
		</div>
	</div>
</div>

<style lang="scss">
	//problem s height:100vh
	.photo-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 1rem;
		width: 100%;
		height: 100%;
	}
</style>
