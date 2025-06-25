<script lang="ts">
	import ProjectPage from '$lib/ProjectPage.svelte';

	import Cover from '$lib/assets/projects/riso/RISO_COVER.jpg';
	import Closeup from '$lib/assets/projects/riso/RISO_Closeup.jpeg';
	import Iteration01 from '$lib/assets/projects/riso/RISO_Iteration01.png';
	import Print01 from '$lib/assets/projects/riso/RISO_Print01.jpeg';
	import Print02 from '$lib/assets/projects/riso/RISO_Print02.jpeg';
	import Sketches from '$lib/assets/projects/riso/RISO_Sketches.jpeg';

	const params = {
		title: 'Risograph Print Project',
		logoImage: Cover,
		images: [
			{ src: Iteration01, alt: 'Iteration01' },
			{ src: Closeup, alt: 'Closeup' },
			{ src: Print02, alt: 'Print02' },
			{ src: Print01, alt: 'Print01' },
			{ src: Sketches, alt: 'Sketches' }
		]
	};
</script>

<ProjectPage {...params}>
	This self directed project was for Second Year Studio at the University of Michigan. Each student
	went through multiple iterations with peer and instructor feedback with the final goal being to
	present in front of a panel of professors. For my project, I wanted to combine multiple things I
	was passionate about, graphic design, nature, and print. I had never used a Risograph machine
	before so I had to figure out how to design specifically for that medium. As well as this, I had
	to figure out the information I wanted to convey and how I wanted to do it.
</ProjectPage>
