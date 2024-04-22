<script lang="ts">
	import { faBars, faArrowLeft } from '@fortawesome/free-solid-svg-icons';
	import Icon from '$lib/Icon.svelte';

	let { showBack } = $props();

	function back() {
		// TODO
	}

	function toggleMenu() {
		// TODO
	}
</script>

<div class="navbar">
	<Icon icon={faArrowLeft} style={'font-size: var(--icon-size);'} onclick={back} />
	<Icon icon={faBars} style={'font-size: var(--icon-size);'} onclick={toggleMenu} />
	<span class="navbar-text">Fiscal Fool</span>
</div>

<style>
	.navbar {
		background-color: var(--color-background-secondary);

		padding: var(--spacing-medium);

		display: flex;
		flex-direction: row;
		justify-content: start;
		gap: var(--spacing-medium);
		align-items: center;
	}

	.navbar-text {
		padding-left: var(--spacing-medium);
		display: flex;
		align-items: center;
		font-size: x-large;
	}
</style>
