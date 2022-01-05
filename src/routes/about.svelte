<script>
</script>

<section class="section">
	<div class="max-width">
		<div class="container">
			<div class="container-text">
				<h1 class="headline">Hello there!</h1>
				<div class="text">
					My name is Liam Walker. I am a professional photographer for 15 years. My name is Liam
					Walker. I am a professional photographer for 15 years. Lorem ipsum dolor sit amet,
					consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore
					magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea
					rebum. Stet clita kasd gubergren, no sea takimata sanctus.
				</div>
			</div>
			<div class="container-image">
				<img src="/images/profile-pic.jpg" alt="profile pic" />
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	.section {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.container {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100%;
		gap: 4rem;

		&-text {
			flex: 1 0 50%;
		}

		&-image {
			height: 80%;
			max-height: 70rem;
			flex: 1 0 40%;

			img {
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
</style>
