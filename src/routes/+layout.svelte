<script>
	import NavBar from './NavBar.svelte';
	import SidePanel from './SidePanel.svelte';
	import './globals.css';
</script>

<div class="app">
	<div class="navbar"><NavBar showBack={true} /></div>
	<div class="sidepanel"><SidePanel isOpen={true} /></div>
	<div class="main"><slot /></div>
</div>

<style>
	.app {
		height: 100%;
		width: 100%;

		color: var(--color-text);
		background-color: var(--color-background-primary);
		border: 1px solid var(--color-text);
	}

	@media (min-width: 768px) {
		.app {
			display: grid;
			grid-template-columns: auto 1fr;
			grid-template-rows: auto 1fr;
			gap: 0px 0px;
			grid-template-areas:
				'NavBar NavBar'
				'SidePanel Main';
		}
	}

	.navbar {
		grid-area: NavBar;

		background-color: var(--color-background-secondary);
	}

	.sidepanel {
		grid-area: SidePanel;

		background-color: var(--color-background-secondary);
	}

	.main {
		grid-area: Main;
	}
</style>
