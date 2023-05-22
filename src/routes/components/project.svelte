<script lang="ts">
	import type { IProject } from 'src/utils/interfaces';
	export let proj: IProject;
</script>

<li class="project-container">
	<a href={proj.url} class="project-link">
		<img
			src={proj.img}
			alt={proj.title}
			class="project-cover"
			style={`background-color: ${proj.bgColor}`}
		/>
		<h1 class="project-title">{proj.title}</h1>
	</a>
</li>

<style>
	.project-container {
		grid-column: span 2;
		grid-row: span 2;
		border: blue solid 2px;
	}
	.project-link {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
		text-decoration: none;
		color: inherit;
	}
	.project-cover {
		width: 80%;
		height: 80%;
		border: solid rgb(255, 0, 0) 1px;
		object-fit: scale-down;
	}
	.project-title {
		height: 20%;
	}
</style>
