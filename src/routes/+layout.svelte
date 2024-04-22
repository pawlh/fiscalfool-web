<script>
	import NavBar from './NavBar.svelte';
	import './globals.css';
</script>

<div class="app">
	<NavBar showBack={true} />
	<slot />
</div>

<style>
	.app {
		height: 100%;
		width: 100%;

		color: var(--color-text);
		background-color: var(--color-background-primary);
	}
</style>
