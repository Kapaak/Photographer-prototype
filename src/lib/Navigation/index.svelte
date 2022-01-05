<nav>
	<div class="max-width">
		<ul>
			<div><a href="/">liamwalker</a></div>
			<li><a href="/overview">overview</a></li>
			<li><a href="/women">women</a></li>
			<li><a href="/men">men</a></li>
			<li><a href="/landscape">landscape</a></li>
			<li><a href="/about">about</a></li>
			<li><a href="/contact">contact</a></li>
		</ul>
	</div>
</nav>

<style lang="scss">
	nav {
		padding: 1rem;
		background-color: var(--col1);
		color: var(--col2);

		ul {
			display: flex;
			gap: 2rem;

			& > div {
				margin-right: auto;
			}

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

			a {
				font-size: inherit;
				text-decoration: none;
				color: inherit;
			}
		}
	}
</style>
