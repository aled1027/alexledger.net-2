<script lang="ts">
	import type { Project } from '$lib/types';
	import ProjectCard from '$lib/components/ProjectCard.svelte';
	import AnnaNeshyba from '$lib/assets/anna-neshyba.png';
	import Metrion from '$lib/assets/metrion.png';
	import Seastar from '$lib/assets/seastar.png';
	import GiveMaxLife from '$lib/assets/give-max-life.png';

	const projects: Project[] = [
		{
			projectName: 'Anna Neshyba',
			imageUrl: AnnaNeshyba,
			imageAlt: 'Screenshot of the Anna Neshyba website'
		},
		{
			projectName: 'Metrion',
			imageUrl: Metrion,
			imageAlt: 'Screenshot of the Metrion website'
		},
		{
			projectName: 'Seastar',
			imageUrl: Seastar,
			imageAlt: 'Screenshot of the Seastar website'
		},
		{
			projectName: 'Give Max Life',
			imageUrl: GiveMaxLife,
			imageAlt: 'Screenshot of the Give Max Life website'
		}
	];
</script>

<section class="hero">
	<h1 class="font-decorative size-step-7">Alex Ledger</h1>
	<div class="size-step-2 mt-2xs">
		<p class="mt-0">
			I'm a web designer and developer from Portland, Oregon. I work with businesses to design and
			build websites.
		</p>
		<p class="mt-m">
			I specialize in creating beautiful, functional websites that help businesses grow. I focus on
			combining good fundamentals— strong, clear copy and design— with a little bit of magic to make
			the experience fun and attention-grabbing.
		</p>
	</div>
</section>
<section>
	<h2 class="small-heading">MY WORK</h2>
	<div class="project-grid mt-l">
		{#each projects as project}
			<ProjectCard {project} />
		{/each}
	</div>
</section>

<style>
	.hero p {
		max-width: 40ch;
	}

	.project-grid {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(30ch, 1fr));
		gap: 1.25rem;
	}

	.small-heading {
		font-size: var(--size-step-0);
		font-weight: var(--font-bold);
		text-transform: uppercase;
		letter-spacing: 0.05em;
	}
</style>
