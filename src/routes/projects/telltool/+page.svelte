<script lang="ts">
	import ProjectPage from '$lib/ProjectPage.svelte';

	import LogoImage from '$lib/assets/projects/telltool/TELLTOOL_Logo.png';

	import Book from '$lib/assets/projects/telltool/TELLTOOL_Book.jpeg';
	import CoverImage from '$lib/assets/projects/telltool/TELLTOOL_CoverImage.jpeg';
	import DesktopLanding from '$lib/assets/projects/telltool/TELLTOOL_DesktopLanding.jpg';
	import DesktopMockup from '$lib/assets/projects/telltool/TELLTOOL_DesktopMockup.png';
	import MobileMockup from '$lib/assets/projects/telltool/TELLTOOL_MobileMockup.png';
	import PosterMockup from '$lib/assets/projects/telltool/TELLTOOL_PosterMockup.png';

	const params = {
		title: 'TELL Tool Visual Identity and Branding',
		logoImage: LogoImage,
		images: [
			{ src: PosterMockup, alt: 'PosterMockup' },
			{ src: Book, alt: 'Book' },
			{ src: DesktopMockup, alt: 'DesktopMockup' },
			{ src: CoverImage, alt: 'CoverImage' },
			{ src: DesktopLanding, alt: 'DesktopLanding' },
			{ src: MobileMockup, alt: 'MobileMockup' }
		]
	};
</script>

<ProjectPage {...params}>
	This project was for my Visual Identity and Branding class at the University of Michigan. The goal
	was for each student to develop a branding identity for Dr. Hershberger’s project, TELL Tool, at
	the University of Michigan’s School of Nursing. The client specified that they wanted to include
	certain colors, like the use of purple for fertility, and an emphasis on inclusivity. For the
	final project, I created a presentation for the client, a visual identity and branding guide, and
	an assortment of collateral so the client could see the branding identity applied in different
	ways.
</ProjectPage>
