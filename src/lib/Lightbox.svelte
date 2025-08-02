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
		<div>
			{#each images as image, index}
				<GalleryThumbnail id={index}>
					<div class="pt-4">
						<img class="w-full border border-slate-800" {...image} />
					</div>
				</GalleryThumbnail>
			{/each}
		</div>
	</svelte:fragment>

	{#each images as { src, alt }}
		<GalleryImage>
			<img {src} {alt} />
		</GalleryImage>
	{/each}
</LightboxGallery>
