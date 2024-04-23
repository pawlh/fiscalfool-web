<script lang="ts">
	type Props = {
		isOpen: boolean;
	};
	let { isOpen }: Props = $props();
</script>

<div class="side-panel" class:visible={isOpen}>
	<div class="side-panel__content">
		<p>here is some content</p>
	</div>
</div>

<style>
	.side-panel {
		display: flex; /* needed to fix margin collapse with children */

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
</style>
