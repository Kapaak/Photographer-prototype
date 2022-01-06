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
	@use '../styles/mixins';

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

		@include mixins.set-breakpoint('tablet') {
			flex-direction: column-reverse;
			gap: 2rem;
		}

		&-text {
			flex: 1 0 50%;
		}

		&-image {
			margin-top: var(--nav-ofst);
			height: 80%;
			max-height: 70rem;
			flex: 1 0 40%;
			transition: all 0.5s;

			@include mixins.set-breakpoint('desktopX') {
				height: 66%;
			}

			@include mixins.set-breakpoint('tablet') {
				height: 20rem;
				width: 100%;
				margin-top: 6rem;
			}
		}
	}
</style>
