<script lang="ts">
	import { LightboxGallery, GalleryThumbnail, GalleryImage } from 'svelte-lightbox';

	const imageModules = import.meta.glob('$lib/assets/portfolio/*{.jpg,png,jpeg,gif}', {
		eager: true
	}) as Record<string, { default: string }>;
	const images = Object.values(imageModules).map((module) => module.default);
</script>

<LightboxGallery>
	<svelte:fragment slot="thumbnail">
		<div class="columns-2 gap-4 lg:columns-4">
			{#each images as image, index}
				<GalleryThumbnail id={index}>
					<div class="pt-4">
						<img class=" w-full border border-slate-800" src={image} alt="thumbnail" />
					</div>
				</GalleryThumbnail>
			{/each}
		</div>
	</svelte:fragment>

	{#each images as image}
		<GalleryImage>
			<img src={image} alt="TODO" />
		</GalleryImage>
	{/each}
</LightboxGallery>
