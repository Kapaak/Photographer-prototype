<script>
	export let photos;
</script>

<main>
	<div class="photo-grid">
		{#each photos as photo, i (i)}
			<div class="box">
				<img src={photo} alt="" />
			</div>
		{/each}
	</div>
</main>

<style lang="scss">
	.photo-grid {
		display: flex;
		width: 100%;
		gap: 1rem;

		.box {
			flex: 1 1 30%;
			height: 18rem;

			img {
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
</style>
