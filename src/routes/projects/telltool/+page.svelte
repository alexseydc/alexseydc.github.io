<script lang="ts">
	import LogoImage from '$lib/assets/projects/telltool/TELLTOOL_Logo.png';

	import Lightbox from '$lib/Lightbox.svelte';
	import Book from '$lib/assets/projects/telltool/TELLTOOL_Book.jpeg';
	import CoverImage from '$lib/assets/projects/telltool/TELLTOOL_CoverImage.jpeg';
	import DesktopLanding from '$lib/assets/projects/telltool/TELLTOOL_DesktopLanding.jpg';
	import DesktopMockup from '$lib/assets/projects/telltool/TELLTOOL_DesktopMockup.png';
	import MobileMockup from '$lib/assets/projects/telltool/TELLTOOL_MobileMockup.png';
	import PosterMockup from '$lib/assets/projects/telltool/TELLTOOL_PosterMockup.png';
	import { layoutState } from '$lib/store.js';

	layoutState.set({ message: 'TELL Tool Visual Identity and Branding' });

	const imageClass = 'mb-4 w-full border-2 border-lime-800';

	const images = [
		{ src: PosterMockup, alt: 'PosterMockup', class: imageClass },
		{ src: Book, alt: 'Book', class: imageClass },
		{ src: DesktopMockup, alt: 'DesktopMockup', class: imageClass },
		{ src: CoverImage, alt: 'CoverImage', class: imageClass },
		{ src: DesktopLanding, alt: 'DesktopLanding', class: imageClass },
		{ src: MobileMockup, alt: 'MobileMockup', class: imageClass }
	];
</script>

<div class="mb-5">
	<div class="flex justify-evenly flex-wrap md:flex-nowrap">
		<div class="w-500 px-10 pt-5">
			<img src={LogoImage} alt="logo" class="h-auto mb-10 w-64 md:w-96 lg:w-full" />
		</div>
		<div class="font-lexend">
			This project was for my Visual Identity and Branding class at the University of Michigan. The
			goal was for each student to develop a branding identity for Dr. Hershberger’s project, TELL
			Tool, at the University of Michigan’s School of Nursing. The client specified that they wanted
			to include certain colors, like the use of purple for fertility, and an emphasis on
			inclusivity. For the final project, I created a presentation for the client, a visual identity
			and branding guide, and an assortment of collateral so the client could see the branding
			identity applied in different ways.
		</div>
	</div>

	<div class="mt-15 columns-2 gap-4 md:columns-4">
		<Lightbox {images} />
	</div>

</div>
