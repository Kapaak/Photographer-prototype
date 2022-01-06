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
		<div class="photo-container">
			<div class="photo filter-grayscale">
				<img src="/images/women/woman5.jpg" alt="wom1" />
			</div>
			<OneRowGrid {photos} />
		</div>
	</div>
</div>

<style lang="scss">
	.photo-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 1rem;
		width: 100%;
		height: 100%;
	}

	.photo {
		height: 69%;
		margin-top: var(--nav-ofst);
	}
</style>
