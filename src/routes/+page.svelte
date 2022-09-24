<script>
	import Info from './components/info.svelte';
</script>

<main class="main">
	<h1>Guillem Sardà Parreu</h1>
	<Info />
</main>

<style>
	.main {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
		height: 100vh;
		width: 100vw;
	}
	h1 {
		font-family: 'Courier New', Courier, monospace;
		transition: 1.5s ease;
		justify-self: center;
	}
	h1:hover {
		color: #ff3e00;
	}
</style>
