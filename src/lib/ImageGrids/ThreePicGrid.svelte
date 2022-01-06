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
		grid-template-columns: repeat(2, 1fr);
		grid-template-rows: repeat(2, 1fr);

		.box {
			//kdyz menim velikost height tady, tak tim ovladam celej container. coz je gut
			height: 18rem;
			//height: calc(20rem + 11vw); zkus

			&:first-of-type {
				height: auto;
				grid-column: 1/2;
				grid-row: 1/3;
			}
		}

		@include mixins.set-breakpoint('mobile') {
			grid-template-columns: repeat(2, 1fr);
			gap: 2rem;
		}
	}
</style>
