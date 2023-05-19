<script lang="ts">
	import type { IProject } from 'src/utils/interfaces';
	export let proj: IProject;
</script>

<li class="project-container">
	<img src="placeholder-image.png" alt={proj.title} class="project-cover" />
	<h1 class="project-title">{proj.title}</h1>
</li>

<style>
	.project-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		border: blue solid 1px;
		grid-column: span 2;
		grid-row: span 2;
	}
	.project-cover {
		width: 100%;
		height: 80%;
	}
	.project-title {
		height: 20%;
	}
</style>
