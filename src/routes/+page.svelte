<script>
	import Carrousel from './components/carrousel.svelte';
</script>

<main class="main">
	<span class="name">
		<h1>Guillem Sardà Parreu</h1>
	</span>
	<Carrousel />
</main>

<style>
	.main {
		display: grid;
		height: 100vh;
		grid-template-columns: repeat(10, 1fr);
		grid-template-rows: repeat(10, 1fr);
	}
	.name {
		display: flex;
		justify-content: center;
		align-items: center;
		grid-column: span 20;
		grid-row: span 2;
	}
	.name > h1 {
		font-weight: 100;
		transition: 0.2s ease;
	}
	.name > h1:hover {
		font-weight: 500;
		color: #ff3e00;
	}
</style>
