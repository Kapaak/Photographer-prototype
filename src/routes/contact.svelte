<div class="section">
	<div class="max-width">
		<div class="container">
			<h1 class="headline">Contact me!</h1>
			<a href="mailto:liamwalker@gmal.com" class="text">liamwalker@gmal.com</a>
		</div>
	</div>
</div>

<style lang="scss">
	@use '../styles/mixins';

	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100%;

		a {
			color: inherit;
		}
	}

	.section {
		@include mixins.set-breakpoint('mobile') {
			height: calc(100vh - var(--nav-ofst));
		}
	}
</style>
