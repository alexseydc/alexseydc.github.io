<script lang="ts">
	import ProjectPage from '$lib/ProjectPage.svelte';

	import Banner from '$lib/assets/projects/filmfestival/AAFF_Banner.png';
	import WIP_01 from '$lib/assets/projects/filmfestival/AAFF_WIP_01.png';
	import WIP_02 from '$lib/assets/projects/filmfestival/AAFF_WIP_02.png';
	import IMG_0914 from '$lib/assets/projects/filmfestival/IMG_0914.png';
	import SocialImage01 from '$lib/assets/projects/filmfestival/SocialImage01.png';
	import SocialImage02 from '$lib/assets/projects/filmfestival/SocialImage02.png';
	import SocialImage03 from '$lib/assets/projects/filmfestival/SocialImage03.png';

	const params = {
		title: 'Ann Arbor Film Festival',
		logoImage: Banner,
		images: [
			{ src: WIP_01, alt: 'WIP_01' },
			{ src: IMG_0914, alt: 'IMG_0914' },
			{ src: SocialImage01, alt: 'SocialImage01' },
			{ src: SocialImage02, alt: 'SocialImage02' },
			{ src: WIP_02, alt: 'WIP_02' },
			{ src: SocialImage03, alt: 'SocialImage03' }
		]
	};
</script>

<ProjectPage {...params}>
	For my senior year at the University of Michigan I interned at the Ann Arbor Film Festival as one
	of two graphic design assistants. Mike, the AAFF’s lead graphic designer, created the assets and
	we worked with them to create different materials used for the festival. I created social media
	graphics, formatted digital advertisements for different websites, and worked together in my team
	to help make the film festival happen.
</ProjectPage>
