<script lang="ts">
	import { FontAwesomeIcon, type FontAwesomeIconProps } from '@fortawesome/svelte-fontawesome';

	type Props = FontAwesomeIconProps & {
		onclick?: (e: any) => void;
	};

	let { onclick, ...props }: Props = $props();
</script>

{#if onclick}
	<button onclick={onclick as (e: any) => void} onkeydown={onclick}>
		<FontAwesomeIcon {...props} />
	</button>
{:else}
	<FontAwesomeIcon {...props} />
{/if}

<style>
	button {
		background: none;
		border: none;
		cursor: pointer;
		color: var(--color-text);
	}
</style>
