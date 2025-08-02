<script lang="ts">
	import Lightbox from '$lib/Lightbox.svelte';
	import { layoutState } from '$lib/store.js';

	interface Image {
		src: string;
		alt: string;
	}

	const { images, logoImage, title, children } = $props<{
		images: Image[];
		title: string;
		logoImage: string;
		children: () => unknown;
	}>();

	layoutState.set({ message: title });
</script>

<div class="mb-5">
	<div class="flex flex-wrap justify-evenly md:flex-nowrap lg:items-center">
		<div class="w-500 px-10 pt-5">
			<img src={logoImage} alt="logo" class="mb-10 h-auto w-64 md:w-96 lg:w-full" />
		</div>
		<div class="font-lexend lg:text-2xl">{@render children()}</div>
	</div>

	<div class="mt-15 columns-2 gap-4 md:columns-3">
		<Lightbox {images} />
	</div>
</div>
