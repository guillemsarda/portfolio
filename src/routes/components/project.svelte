<script lang="ts">
	import type { IProject } from 'src/utils/interfaces';
	export let proj: IProject;
</script>

<li class="project-container">
	<a href={proj.url} class="project-link" target="_blank">
		<img
			src={proj.img}
			alt={proj.title}
			class="project-cover"
			style={`background-color: ${proj.bgColor}`}
		/>
		<span class="project-title">
			<h1>{proj.title}</h1>
		</span>
	</a>
</li>

<style>
	@keyframes bounce {
		50% {
			transform: translateY(-15px);
		}
		100% {
			transform: translateY(0);
		}
	}
	.project-container {
		grid-column: span 2;
		grid-row: span 2;
		display: flex;
		align-items: center;
		justify-content: center;
		opacity: 0.6;
		transition: all ease-out 0.5s;
	}
	.project-container:hover {
		opacity: 1;
		animation: bounce 3s infinite ease-out;
	}
	.project-link {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 80%;
		height: 100%;
		text-decoration: none;
		color: inherit;
	}
	.project-cover {
		width: 100%;
		height: 75%;
		border: solid var(--grey) 3px;
		border-bottom: none;
		border-radius: 20px 20px 0px 0px;
		object-fit: scale-down;
	}
	.project-title {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 25%;
		border: solid var(--grey) 3px;
		border-top: none;
		border-radius: 0px 0px 20px 20px;
	}
	.project-title h1 {
		font-size: 1.5rem;
		font-weight: 400;
	}
</style>
