<script>
	import Hamburger from './Hamburger.svelte';

	$: toggle = false;

	const toggleHandler = (trigger) => {
		toggle = trigger.detail.toggle;
	};

	const colapseMenu = () => {
		toggle = !toggle;
	};
</script>

<nav>
	<div class="max-width" aria-expanded={toggle.toString()}>
		<div class="logo">
			<Hamburger on:toggle={toggleHandler} {toggle} />
			<a href="/">liamwalker</a>
		</div>
		<ul aria-expanded={toggle.toString()}>
			<li on:click={colapseMenu}><a href="/">overview</a></li>
			<li on:click={colapseMenu}><a href="/women">women</a></li>
			<li on:click={colapseMenu}><a href="/men">men</a></li>
			<li on:click={colapseMenu}><a href="/landscape">landscape</a></li>
			<li on:click={colapseMenu}><a href="/about">about</a></li>
			<li on:click={colapseMenu}><a href="/contact">contact</a></li>
		</ul>
	</div>
</nav>

<style lang="scss">
	@use '../../styles/mixins';

	.max-width {
		display: flex;
		justify-content: space-between;

		&[aria-expanded='true'] {
			height: 100vh;
		}
	}

	nav {
		position: fixed;
		width: 100%;
		padding: 1rem 0;
		background-color: var(--col1);
		color: var(--col2);

		.logo {
			@include mixins.set-breakpoint('tablet') {
				display: flex;
				flex-flow: row-reverse;
				justify-content: space-between;
				align-items: center;
				height: 3rem;
				width: 100%;
			}
		}

		ul {
			display: flex;
			gap: 2rem;

			li {
				position: relative;
				display: flex;
				align-items: center;
				list-style-type: none;
				font-size: 1.4rem;

				&::before {
					position: absolute;
					content: '';
					width: 0%;
					background-color: var(--col2);
					height: 0.2rem;
					transition: all 0.3s ease;
					pointer-events: none;
				}

				&:hover {
					a {
						transition: all 0.3s ease;
						opacity: 0.4;
					}

					&::before {
						width: 100%;
						transition: all 0.3s ease;
					}
				}
			}

			@include mixins.set-breakpoint('tablet') {
				display: none;
				position: absolute;
				flex-direction: column;
				height: 100vh;
				justify-content: center;

				&[aria-expanded='true'] {
					display: flex;
				}
			}
		}
		a {
			font-size: inherit;
			text-decoration: none;
			color: inherit;
		}
	}
</style>
