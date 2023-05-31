<script lang="ts">
	import { fly, fade } from 'svelte/transition';
	let visible = 'beginning';
	interface currentToNextVisibleInt {
		beginning: string;
		stack: string;
	}

	const currentToNextVisible: currentToNextVisibleInt = {
		beginning: 'stack',
		stack: 'next'
	};

	function handleClick() {
		visible = currentToNextVisible[visible as keyof currentToNextVisibleInt] ?? 'beginning';
	}
</script>

<button class="info-button" on:click={handleClick}>
	{#if visible === 'beginning'}
		<p class="intro-content" in:fade={{ duration: 1000 }}>
			I am a Software Developer (click for more).
		</p>
	{:else if visible === 'stack'}
		<p class="intro-content" in:fly={{ x: -500, duration: 1000 }}>
			I am proficient with JavaScript and TypeScript (click for more).
		</p>
	{:else if visible === 'next'}
		<p class="intro-content" in:fly={{ x: -500, duration: 1000 }}>
			Currently learning C. Stay tuned (click to end).
		</p>
	{/if}
</button>

<style>
	.info-button {
		width: auto;
		background-color: transparent;
		border: none;
	}
	.intro-content {
		font-family: 'Courier New', Courier, monospace;
	}
</style>
