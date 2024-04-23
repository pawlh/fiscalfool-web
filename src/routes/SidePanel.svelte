<script lang="ts">
	type Props = {
		isOpen: boolean;
	};
	let { isOpen }: Props = $props();
</script>

<div class="side-panel" class:visible={isOpen}>
	<div class="side-panel__content">
		<!-- <header class="side-panel__header">
			<h1>Here is a header</h1>
		</header> -->
		<div class="side-panel__container">
			<p>here is some content</p>
		</div>
	</div>
</div>

<style>
	.side-panel {
		display: flex; /*  */

		visibility: hidden;
		transition: visibility 0s 0.6s;

		height: 100%;

		&.visible {
			visibility: visible;
			transition: visibility 0s 0s;
		}
	}

	@media (min-width: 768px) {
		.side-panel {
			visibility: visible;
			transition: visibility 0s 0s;
		}
	}

	.side-panel__content {
		position: fixed;
		top: 0;
		left: 0;

		width: 80%;
		height: 100%;

		transition: transform 0.3s 0s;
		transform: translate3d(-100%, 0, 0);

		background-color: var(--color-background-secondary);

		.visible & {
			transform: translate3d(0, 0, 0);
			transition-delay: 0s;
		}
	}

	@media (min-width: 768px) {
		.side-panel__content {
			position: static;
			width: 20vw;
		}
	}

	.side-panel__header {
		border-bottom: 1px solid var(--color-text);

		h1 {
			font-size: 1.5rem;
			margin: 0;
			padding: 1rem;
		}
	}
</style>
