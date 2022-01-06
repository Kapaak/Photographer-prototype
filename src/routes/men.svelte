<script>
	import FourPicGrid from '$lib/ImageGrids/FourPicGrid.svelte';

	const photos = [
		'/images/men/man2.jpg',
		'/images/men/man1.jpg',
		'/images/men/man3.jpg',
		'/images/men/man4.jpg'
	];
</script>

<div class="section">
	<div class="max-width">
		<div class="photo-container">
			<FourPicGrid {photos} />
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
