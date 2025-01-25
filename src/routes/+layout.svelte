<script lang="ts">
	import '../app.css';
	let { children } = $props();
	import Footer from '$lib/comps/Footer.svelte';
</script>

<main class="relative">
	{@render children()}
	<Footer />
</main>
