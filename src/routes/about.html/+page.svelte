<script>
	import { base } from '$app/paths';
	import { browser } from '$app/environment';

	if (browser) {
		window.location.href = `${base}/about-me`;
	}
</script>
