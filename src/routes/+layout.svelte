<script lang="ts">
	import '../app.css';

	let { children } = $props();
	import { dev } from '$app/environment';
	import { injectAnalytics } from '@vercel/analytics/sveltekit';

	injectAnalytics({ mode: dev ? 'development' : 'production' });
</script>

{@render children()}
