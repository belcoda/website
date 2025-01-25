<script lang="ts">
	import { page } from '$app/state';
	import Nav from '$lib/comps/Nav.svelte';
</script>

<Nav />
<svelte:head>
	<title>Error - Belcoda</title>
</svelte:head>
<section class="isolate bg-gray-100 px-6 py-24 sm:py-32 lg:px-8 lg:pb-32 lg:pt-40">
	<div class="mx-auto max-w-2xl text-center">
		<h2 class="text-balance text-4xl font-extrabold tracking-tight text-gray-800 sm:text-5xl">
			{page.status}
		</h2>
		<p class="mt-2 text-lg/8 text-gray-600">
			{page?.error?.message || 'An error occurred. Please try again later.'}
		</p>
	</div>
	<div class="mx-auto mt-10 max-w-md text-center">
		<a
			href="/"
			class="shadow-xs block w-full rounded-md bg-gray-800 px-3.5 py-2.5 text-center text-sm font-semibold text-white hover:bg-gray-700 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
		>
			Back to Home
		</a>
	</div>
</section>
