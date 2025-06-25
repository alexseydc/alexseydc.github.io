<script lang="ts">
	import ProjectPage from '$lib/ProjectPage.svelte';

	import branding from '$lib/assets/projects/botanical/matthaeibranding_2.png';
	import branding01 from '$lib/assets/projects/botanical/matthaei branding-01.jpg';
	import branding03 from '$lib/assets/projects/botanical/matthaei branding-03.jpg';
	import branding04 from '$lib/assets/projects/botanical/matthaei branding-04.jpg';
	import sketches from '$lib/assets/projects/botanical/matthaei_sketches.jpg';

	const params = {
		title: 'Matthaei Botanical Gardens Redesign',
		logoImage: sketches,
		images: [
			{ src: branding, alt: 'branding' },
			{ src: branding01, alt: 'branding01' },
			{ src: branding03, alt: 'branding03' },
			{ src: branding04, alt: 'branding04' }
		]
	};
</script>

<ProjectPage {...params}>
	For my Poster Design class at the University of Michigan my professor had us redesign the Matthaei
	Botanical Garden’s visual identity. This consisted of a poster, banner, and business cards. For my
	design, I was experimenting with something more modular that could be used as a border or placed
	on merchandise. I wanted to be able to take apart the design and it to still work and be complete.
	Each of the flowers in the poster are sketches of the flowers that are in the greenhouse at the
	botanical gardens.
</ProjectPage>
