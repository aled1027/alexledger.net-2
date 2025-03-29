<script lang="ts">
	import type { Project } from '$lib/types';
	let { project }: { project: Project } = $props();
</script>

<div class="project-card">
	<div class="project-card__title-wrapper">
		<h3 class="project-card__title">{project.projectName}</h3>
	</div>
	<div class="project-card__middle-entry project-card__scale-animation padding-4">
		<div class="project-card__asset-wrapper">
			<img class="project-card__cover-asset" src={project.imageUrl} alt={project.imageAlt} />
		</div>
	</div>
</div>

<style>
	.project-card {
		--light-purple: hsl(255.65, 45%, 90%);
		--dark-purple: hsl(255.65, 45%, 30%);
		--card-border-color: var(--dark-purple);
		--card-border-color-light: hsl(from var(--dark-purple) h s l / 0.2);
		--card-bg-color: hsl(from var(--light-purple) h s l / 0.6);

		background: var(--card-bg-color);
		border: 0.125px solid var(--card-border-color);
		border-radius: 4px;
		width: 100%;
		box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.1);
		overflow: hidden;

		display: flex;
		flex-direction: column;
		justify-content: space-between;
		gap: 0;
	}

	.project-card__title-wrapper {
		padding: 1rem;
		border-bottom: 0.5px solid var(--card-border-color-light);
	}

	.project-card__title {
		font-size: var(--size-step-0);
		text-decoration: none;
	}

	.project-card__asset-wrapper {
		width: 100%;
		aspect-ratio: 16 / 9;
		border-bottom-left-radius: 4px;
		border-bottom-right-radius: 4px;
		overflow: hidden;
		position: relative;

		transition:
			transform 0.3s ease-in-out,
			filter 0.3s ease-in-out;
	}

	.project-card:hover .project-card__asset-wrapper {
		transform: scale(1.03);
		filter: brightness(1.05);
	}
</style>
