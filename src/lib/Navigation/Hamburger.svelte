<script>
	export let toggle;

	import { createEventDispatcher } from 'svelte';
	const dispatch = createEventDispatcher();
	const toggleHandler = () => {
		toggle = !toggle;
		dispatch('toggle', {
			toggle
		});
	};
</script>

<div on:click={toggleHandler}>
	<p />
	<p />
	<p />
</div>

<style lang="scss">
	@use '../../styles/mixins';

	div {
		display: none;
		flex-direction: column;
		justify-content: space-between;
		width: 2.6rem;
		height: 2rem;
		cursor: pointer;

		@include mixins.set-breakpoint('tablet') {
			display: flex;
		}
	}

	p {
		width: 100%;
		height: 0.2rem;
		background-color: var(--col2);
	}
</style>
