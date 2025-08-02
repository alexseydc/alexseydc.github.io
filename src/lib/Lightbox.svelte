<script lang="ts">
	import { LightboxGallery, GalleryThumbnail, GalleryImage } from 'svelte-lightbox';

	interface Image {
		src: string;
		alt: string;
	}

	const { images } = $props<{ images: Image[] }>();
</script>

<LightboxGallery>
	<svelte:fragment slot="thumbnail">
		{#each images as image, index}
			<GalleryThumbnail id={index}>
				<div class="inline-block pb-4">
					<img class="w-full border border-slate-800" {...image} />
				</div>
			</GalleryThumbnail>
		{/each}
	</svelte:fragment>

	{#each images as { src, alt }}
		<GalleryImage>
			<img {src} {alt} />
		</GalleryImage>
	{/each}
</LightboxGallery>

<style>
	:global(div.svelte-lightbox-body button) {
		cursor: pointer;
	}

	:global(div.svelte-lightbox-body svg) {
		background-color: rgba(200, 200, 200, 0.3);
		border-radius: 50%;
	}

	:global(div.svelte-lightbox-body button:disabled) {
		display: none;
		pointer-events: none;
	}
</style>
