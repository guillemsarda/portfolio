<script lang="ts">
	import Project from './project.svelte';
	const arr = [
		{
			title: 'Parkpal',
			url: 'https://parkpal-web-omega.vercel.app/',
			img: '/parkpal-logo.svg',
			bgColor: 'rgb(113,69,214)'
		},
		{
			title: 'react-rxjs-state-management',
			url: 'https://www.npmjs.com/package/react-rxjs-state-management',
			img: '/npm.svg',
			bgColor: 'rgb(193,32,39)'
		},
		{
			title: 'What2Do',
			url: 'https://github.com/guillemsarda/what2do',
			img: '/w2d.png',
			bgColor: 'rgb(217,240,252)'
		},
		{
			title: 'Bienvenido Al Globo',
			url: 'https://www.bienvenidoalglobo.top/',
			img: '/globo-logo.svg',
			bgColor: 'rgb(248, 249, 250)'
		}
	];
</script>

<ul class="carrousel">
	{#each arr as proj}
		<Project {proj} />
	{/each}
</ul>

<style>
	.carrousel {
		display: grid;
		grid-row: span 7;
		grid-column: 2 / 10;
		list-style-type: none;
		grid-template-columns: repeat(4, 1fr);
		grid-template-rows: repeat(4, 1fr);
		row-gap: 5vh;
		column-gap: 15vw;
	}
</style>
