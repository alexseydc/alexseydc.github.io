<script lang="ts">
	import { LightboxGallery, GalleryThumbnail, GalleryImage } from 'svelte-lightbox';

	// let { images } = $props();
    interface Image {
        src: string;
        alt: string;
        class: string;
    }

    export let images: Image[];
</script>

<LightboxGallery>
	<svelte:fragment slot="thumbnail">
		<div>
			{#each images as image, index}
				<GalleryThumbnail id={index}>
					<img {...image} />
				</GalleryThumbnail>
			{/each}
		</div>
	</svelte:fragment>

	{#each images as {src, alt}}
		<GalleryImage>
			<img src={src} alt={alt} />
		</GalleryImage>
	{/each}
</LightboxGallery>
