<div class="side-panel visible">
	<header class="side-panel__header">
		<h1>Here is a header</h1>
	</header>
	<div class="side-panel__container">
		<p>here is some content</p>
	</div>
</div>

<style>
	.side-panel {
		visibility: hidden;
		transition: visibility 0s 0.6s;

		&.visible {
			visibility: visible;
			transition: visibility 0s 0s;
		}
	}

	.side-panel__header {
		position: fixed;
		top: 0;
		left: 0;

		width: 80%;
		height: 50px;

		transition: transform 0.3s 0s;
		transform: translateY(-50px);

		/* centered partial border on bottom */
		border-bottom: 1px solid var(--color-text);

		.visible & {
			transition: transform 0.3s 0.3s;
			transform: translateY(0px);
		}
	}

	.side-panel__container {
		position: fixed;
		top: 50px;
		left: 0;

		width: 80%;
		height: 100%;

		transition: transform 0.3s 0s;
		transform: translate3d(-100%, 0, 0);

		.visible & {
			transform: translate3d(0, 0, 0);
			transition-delay: 0s;
		}
	}

	.side-panel > * {
		background-color: var(--color-background-secondary);
		color: var(--color-text);
	}
</style>
