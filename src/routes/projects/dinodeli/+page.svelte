<script lang="ts">
	import ProjectPage from '$lib/ProjectPage.svelte';

	import CoverImage from '$lib/assets/projects/dinodeli/DINODELI_CoverImage.jpeg';
	import BoxFlat from '$lib/assets/projects/dinodeli/DINODELI_BoxFlat.jpeg';
	import DesktopMockup from '$lib/assets/projects/dinodeli/DINODELI_DesktopMockup.jpg';
	import Hotsauce from '$lib/assets/projects/dinodeli/DINODELI_Hotsauce.jpeg';
	import Hotsauce02 from '$lib/assets/projects/dinodeli/DINODELI_Hotsauce02.jpeg';
	import Logo from '$lib/assets/projects/dinodeli/DINODELI_Logo.png';
	import Menu from '$lib/assets/projects/dinodeli/DINODELI_Menu.png';
	import MobileMockup from '$lib/assets/projects/dinodeli/DINODELI_MobileMockup.png';
	import Poster01 from '$lib/assets/projects/dinodeli/DINODELI_Poster01.png';
	import wallsign from '$lib/assets/projects/dinodeli/DINODELI_wallsign.png';

	const params = {
		title: 'Dino Deli',
		logoImage: Logo,
		images: [
			{ src: BoxFlat, alt: 'BoxFlat' },
			{ src: DesktopMockup, alt: 'DesktopMockup' },
			{ src: Hotsauce, alt: 'Hotsauce' },
			{ src: Hotsauce02, alt: 'Hotsauce02' },
			{ src: CoverImage, alt: 'CoverImage' },
			{ src: Menu, alt: 'Menu' },
			{ src: MobileMockup, alt: 'MobileMockup' },
			{ src: Poster01, alt: 'Poster01' },
			{ src: wallsign, alt: 'wallsign' }
		]
	};
</script>

<ProjectPage {...params}>
	I decided to do this project for my Narrative Forms class at the University of Michigan. The goal
	was to tell a story from start to finish using any medium. The goal of graphic design is to tell a
	story and communicate information to your viewer so I felt that this is where I could really
	shine. I wanted to create a Deli that was themed around the geological time scale. I created a
	logo, menu, website landing page, and some packaging designs for a well rounded story. This
	project challenged me because it was self directed and I found that was something I really
	enjoyed.
</ProjectPage>
