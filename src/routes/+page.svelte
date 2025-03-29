<script lang="ts">
	import Accordion from '$lib/components/Accordion.svelte';
</script>

<section class="grid" data-layout="50-50">
	<div>
		<h1>Metrion</h1>
		<p>
			Artificial intelligence and geospatial data driven insights for a resilient and sustainable
			future
		</p>
		<a class="button" href="/contact" data-bigger> Book Consultation </a>
	</div>
	<enhanced:img src="../../src/lib/assets/globe.png" alt="The earth from space" class="globe" />
</section>
<section>
	<p>
		At Metrion, we turn complex geospatial data into actionable intelligence, helping organizations
		navigate risk and opportunity in a changing world. With expertise in real estate, disaster
		response, and environmental modeling, we provide data-driven insights to future-proof assets and
		operations.
	</p>
</section>

<section>
	<h2>Services</h2>
	<div class="mt-l">
		<Accordion />
	</div>
</section>
