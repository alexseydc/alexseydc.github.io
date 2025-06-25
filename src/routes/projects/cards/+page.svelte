<script lang="ts">
	import ProjectPage from '$lib/ProjectPage.svelte';

	import CoverImage from '$lib/assets/projects/cards/CARDS_CoverImage.png';
	import cards1 from '$lib/assets/projects/cards/cards1.jpg';
	import flat from '$lib/assets/projects/cards/cards_flat.png';

	const params = {
		title: 'Playing Cards Project',
		logoImage: CoverImage,
		images: [
			{ src: CoverImage, alt: 'CoverImage' },
			{ src: cards1, alt: 'cards1' },
			{ src: flat, alt: 'flat' }
		]
	};
</script>

<ProjectPage {...params}>
	This project I made during a beginner illustrator course. It started out as the first set of cards
	in red at the bottom and then I wanted to take it and rework what I had already done. This project
	was when i really started exploring connecting graphic design to something I was really passionate
	about, wildlife and animals. When I realized I could create things that someone could potentially
	use and interact with it really inspired me and built my passion for graphic design.
</ProjectPage>
