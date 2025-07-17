<script lang="ts">
	import '../app.css';
	import { slide } from 'svelte/transition';
	import { cubicInOut } from 'svelte/easing';
	import { afterNavigate } from '$app/navigation';
	import { base } from '$app/paths';
	import Logo from '$lib/assets/LEXLOGO-01.svg';
	import { layoutState } from '$lib/store.js';
	import Instagram from '$lib/assets/instagram.svg';
	import LinkedIn from '$lib/assets/linkedin.svg';
	import NavItem from '$lib/NavItem.svelte';

	let isDropdownHidden = $state(true);

	function toggleDropdown() {
		isDropdownHidden = !isDropdownHidden;
		console.log('dropdown triggered');
	}

	// Resets mobile nav dropdown on navigation
	afterNavigate(() => {
		isDropdownHidden = true;
	});

	let { children } = $props();
</script>

<div class="min-h-screen bg-amber-50 p-3 lg:p-5">
	<div class="border-2 border-slate-800 px-5 lg:px-20 lg:py-12">
		<!-- desktop -->
		<div class="mb-20 hidden w-full justify-between lg:flex">
			<div class="w-1/4">
				<a href={`${base}/`} class="group flex gap-x-10">
					<img src={Logo} alt="logo" class="h-16 w-16" />
					<div class="">
						<span
							class="
                        font-header
                        text-xl
                        font-medium
                        text-slate-800

                        transition-all
                        group-hover:font-bold
                        lg:text-2xl
                        xl:text-3xl
                        ">Alexsey daCosta</span
						>
						<div
							class="mt-4 w-full border-b-2 border-slate-800 transition-all group-hover:w-[150%]"
						></div>
					</div>
				</a>
			</div>
			<div class="">
				<div class="flex flex-wrap justify-end gap-5">
					<NavItem name={'Home'} href={`${base}/`} />
					<NavItem name={'My work'} href={`${base}/portfolio`} />
					<NavItem name={'About me'} href={`${base}/about-me`} />
				</div>
			</div>
		</div>

		<!-- mobile -->
		<div class="mt-2 mb-8 flex justify-between border-b border-slate-800 pb-2 lg:hidden">
			<div>
				<a href={`${base}/`} class="group flex items-center gap-x-10">
					<img src={Logo} alt="logo" class="h-10 w-10" />
					<span class="font-header col-span-3 text-xl font-medium text-slate-800"
						>Alexsey<br />daCosta</span
					>
				</a>
			</div>
			<button onclick={toggleDropdown} class="cursor-pointer pl-5 text-xl text-slate-800">
				{#if isDropdownHidden}
					<!-- <i class="text-slate-800 text-xl fa-solid fa-bars"></i> -->
					<span class="text-5xl text-slate-800">+</span>
				{:else}
					<!-- <i class="text-slate-800 text-xl fa-solid fa-xmark"></i> -->
					<span class="inline-block rotate-45 transform text-5xl text-slate-800">+</span>
				{/if}
			</button>
		</div>
		{#if !isDropdownHidden}
			<div
				transition:slide={{ duration: 500, easing: cubicInOut }}
				class="mb-5 grid grid-cols-1 border-b-2 border-slate-800"
			>
				<a
					href={`${base}/`}
					class="font-header mx-2 mt-2 border-b border-slate-800 pb-2 text-xl font-medium">Home</a
				>
				<a
					href={`${base}/portfolio`}
					class="font-header mx-2 mt-2 border-b border-slate-800 pb-2 text-xl font-medium"
					>My work</a
				>
				<a href={`${base}/about-me`} class="font-header mx-2 mt-2 pb-10 text-xl font-medium"
					>About me</a
				>
			</div>
		{/if}

		<div class="mb-15 flex items-center">
			<div class="font-header text-lg text-nowrap md:text-xl">{$layoutState.message}</div>
			<div class="ml-10 w-full border-b-2 border-slate-800"></div>
		</div>
		{@render children()}

		<!-- footer -->
		<div class="w-full">
			<div
				class="mt-4 w-full border-b-2 border-slate-800 transition-all group-hover:w-[150%]"
			></div>
			<div class="my-5 flex items-center justify-between">
				<div class="flex gap-2">
					<a href="https://www.instagram.com/alexseydc/" target="_blank">
						<img class="h-8" alt="Instagram" src={Instagram} />
					</a>
					<a href="https://www.linkedin.com/in/alexsey-dacosta-8a18b12b1/" target="_blank">
						<img class="h-8" alt="LinkedIn" src={LinkedIn} />
					</a>
				</div>
				<a href={`${base}/`} class="">
					<img src={Logo} alt="logo" class="h-10 w-10" />
				</a>
			</div>
		</div>
	</div>
</div>
