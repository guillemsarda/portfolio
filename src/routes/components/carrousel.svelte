<script lang="ts">
	import Project from './project.svelte';

	const arr = [{ title: 'hello' }, { title: 'world' }, { title: 'hello' }, { title: 'hello' }];
</script>

<ul class="carrousel">
	{#each arr as proj, i}
		<Project {proj} {i} />
	{/each}
	<!-- <li class="project-container fa">h</li>
	<li class="project-container s">h</li>
	<li class="project-container t ">h</li>
	<li class="project-container l">h</li> -->
</ul>

<style>
	.carrousel {
		border: red solid 1px;
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
