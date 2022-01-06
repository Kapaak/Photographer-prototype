<script>
	export let photos;
</script>

<main>
	<div class="photo-grid">
		{#each photos as photo, i (i)}
			<div class="box filter-grayscale">
				<img src={photo} alt="" />
			</div>
		{/each}
	</div>
</main>

<style lang="scss">
	@use '../../styles/mixins';

	.photo-grid {
		display: grid;
		width: 100%;
		gap: 1rem;
		grid-template-columns: repeat(4, 1fr);

		.box {
			height: 18rem;
		}

		@include mixins.set-breakpoint('mobile') {
			grid-template-columns: repeat(2, 1fr);
			gap: 2rem;
		}
	}
</style>
