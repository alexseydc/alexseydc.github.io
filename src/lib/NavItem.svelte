<script lang="ts">
	import { base } from '$app/paths';

	let { name, href } = $props();
</script>

<div class="w-35">
	<a {href} class="group cursor-pointer">
		<div class="grid grid-cols-[auto_25px] border-0">
			<div
				class="
            border-b-2 border-slate-800
            pb-4
            text-xl
            whitespace-nowrap
            text-slate-800

            transition-all
            font-header
            font-medium
            group-hover:font-bold
            lg:text-2xl
            xl:text-3xl"
			>
				{name}
			</div>
			<div
				class="
            mt-4
            w-0
            border-b-2
            border-slate-800
            transition-all
            ease-in-out
            group-hover:w-full
            "
			></div>
		</div>
	</a>
</div>
