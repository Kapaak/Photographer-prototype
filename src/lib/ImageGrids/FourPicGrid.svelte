<script>
	export let photos;
</script>

<div class="photo-grid">
	{#each photos as photo, i (i)}
		<div class="box filter-grayscale">
			<img src={photo} alt="" />
		</div>
	{/each}
</div>

<style lang="scss">
	@use '../../styles/mixins';

	.photo-grid {
		display: grid;
		width: 100%;
		gap: 1rem;
		grid-template-columns: 1fr 15% 1fr;
		grid-template-rows: 1fr 1fr;
		/* height: 40rem; */

		.box {
			height: 30rem;

			&:first-of-type {
				grid-column: 1/3;
				grid-row: 1;
			}

			&:nth-of-type(2) {
				grid-column: 3;
				grid-row: 1;
			}

			&:nth-of-type(3) {
				grid-column: 1/2;
				grid-row: 2;
			}
			&:nth-of-type(4) {
				grid-column: 2/4;
				grid-row: 2;
			}
		}

		/* @include mixins.set-breakpoint('mobile') {
			grid-template-columns: repeat(2, 1fr);
			gap: 2rem;
		} */
	}
</style>
