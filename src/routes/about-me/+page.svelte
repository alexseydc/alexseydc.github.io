<script>
	import Me from '$lib/assets/about-me/MEPICTURE.jpg';
	import { layoutState } from '$lib/store.js';

	layoutState.set({ message: 'About me' });
</script>

<div class="grid grid-cols-1 justify-items-center gap-15 lg:grid-cols-2 lg:gap-40">
	<div class="mx-auto max-w-2xl">
		<!-- <img src={Me} alt="me" class="border-2 border-slate-800 max-w-lg justify-self-end"/> -->
		<img src={Me} alt="me" class="h-auto w-64 border-2 border-slate-800 md:w-96 lg:w-full" />
	</div>
	<div>
		<p class="font-lexend max-w-xl place-self-center justify-self-start text-lg lg:text-xl">
			Hi! My name is Alexsey daCosta and I am a Graphic Designer. I have a BA from the University of
			Michigan where I studied Art & Design.
			<br /><br />
			I am passionate about the environment and all things creative. In my free time you can find me
			taking walks, birdwatching, or playing video games.
			<br /><br />
			If you like what you see I would love to work with you!
		</p>
		<iframe
			class="mt-10"
			title="contact"
			src="https://docs.google.com/forms/d/e/1FAIpQLSe5FNnOkNnH7ltdu_enzeoaF1-1U1Leg8gh7xRUgrU_vKeTmw/viewform?embedded=true"
			width="500"
			height="650"
			frameborder="0"
			marginheight="0"
			marginwidth="0">Loading…</iframe
		>
	</div>
</div>
