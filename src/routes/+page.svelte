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
			imageAlt: 'Screenshot of the Anna Neshyba website',
			cardColor: '#D3DCD9'
		},
		{
			projectName: 'Metrion',
			imageUrl: Metrion,
			imageAlt: 'Screenshot of the Metrion website',
			cardColor: '#8992cb'
		},
		{
			projectName: 'Give Max Life',
			imageUrl: GiveMaxLife,
			imageAlt: 'Screenshot of the Give Max Life website',
			cardColor: '#9335D1'
		},
		{
			projectName: 'Seastar',
			imageUrl: Seastar,
			imageAlt: 'Screenshot of the Seastar website',
			cardColor: '#AAB199'
		}
	];
</script>

<section class="hero">
	<h1 class="font-decorative size-step-7">Alex Ledger</h1>
	<div class="size-step-2 mt-2xs hero-fade-in">
		<p class="mt-0">
			I'm a web designer and developer from Portland, Oregon. I work with businesses to design and
			build websites.
		</p>
		<p class="mt-m">
			I specialize in creating beautiful, functional websites that help businesses grow. I focus on
			combining good fundamentals— strong, clear copy and design— with a sprinkle of magic to make
			the experience fun and attention-grabbing.
		</p>
	</div>
</section>
<section>
	<h2 class="small-heading">MY WORK</h2>
	<div class="project-grid mt-l">
		{#each projects as project}
			<ProjectCard {project} cardColor={project.cardColor} />
		{/each}
	</div>
</section>
<section class="center-children mt-3xl">
	<!-- TODO: maybe write in web component so it doesn't inherit css -->
	<script
		async
		data-uid="da73872bd8"
		src="https://alex-ledger.kit.com/da73872bd8/index.js"
	></script>
</section>

<style>
	.hero p {
		max-width: 40ch;
		line-height: 1.4;
		text-wrap: pretty;
	}

	.hero-fade-in {
		opacity: 0;
		animation: fadeIn 1s forwards;
		transform: translateY(100px);
	}

	@keyframes fadeIn {
		to {
			opacity: 1;
			transform: translateY(0);
		}
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
