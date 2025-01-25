<script lang="ts">
	import Nav from '$lib/comps/Nav.svelte';
	import { IsInViewport } from 'runed';
	let topSection = $state<HTMLElement>()!;
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';
	const topSectionInViewport = new IsInViewport(() => topSection);
	let showNav = $state(false);
	onMount(() => {
		setTimeout(() => (showNav = true), 300);
	});

	let contentSection = $state<HTMLElement>();
	import HeartHandshake from 'lucide-svelte/icons/heart-handshake';
	import HandCoins from 'lucide-svelte/icons/hand-coins';
	import ShieldCheck from 'lucide-svelte/icons/shield-check';
</script>

<svelte:head>
	<title>Belcoda - Software for social change</title>
</svelte:head>

{#if showNav}<div transition:fade={{ duration: 300 }}>
		<Nav hideBackground={topSectionInViewport.current} />
	</div>{/if}
<section
	bind:this={topSection}
	class="background-learning flex min-h-screen items-center justify-center bg-gray-900 bg-cover bg-center md:bg-center"
>
	<div class="container mx-auto px-4 text-center">
		<div class="mx-auto -mt-8 max-w-4xl">
			<div>
				<div class="mb-8 flex justify-center">
					<img src="/logos/white_logomark.svg" alt="Belcoda Foundation logo" class="h-7 w-auto" />
				</div>
				<h2
					class="mb-8 text-3xl font-extrabold tracking-wide text-white md:mb-6 md:text-3xl lg:mb-8 xl:text-4xl"
				>
					Everyone working to make the world a better place should have the software they need to
					succeed.
				</h2>

				<button
					class="text-white hover:scale-125 hover:text-white"
					onclick={() => contentSection?.scrollIntoView({ behavior: 'smooth' })}
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="32"
						height="32"
						viewBox="0 0 24 24"
						fill="none"
						stroke="currentColor"
						stroke-width="0.7"
						stroke-linecap="round"
						stroke-linejoin="round"
						class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6" /></svg
					>
					<span class="sr-only">Scroll down</span>
				</button>
			</div>
		</div>
	</div>
</section>

<div
	bind:this={contentSection}
	class="relative isolate overflow-hidden bg-slate-50 px-6 py-24 sm:py-32 lg:overflow-visible lg:px-0"
>
	<div
		class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 lg:mx-0 lg:max-w-none lg:grid-cols-2 lg:items-start lg:gap-y-6"
	>
		<div
			class="lg:col-span-2 lg:col-start-1 lg:row-start-1 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8"
		>
			<div class="lg:pr-4">
				<div class="lg:max-w-lg">
					<h1
						class="mt-2 text-pretty text-4xl font-extrabold tracking-tight text-gray-900 sm:text-5xl"
					>
						Software for community leaders
					</h1>
					<p class="mt-6 text-xl/8 text-gray-700">
						Software should empower social change. But the people working to create change are being
						held back by software that doesn’t meet their needs.
					</p>
				</div>
			</div>
		</div>
		<div
			class="-ml-12 -mt-12 p-12 lg:sticky lg:top-[10%] lg:col-start-2 lg:row-span-2 lg:row-start-1 lg:overflow-hidden"
		>
			<img
				class="w-[48rem] max-w-none rounded-md shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem]"
				src="/images/desktop.png"
				alt="Screenshot of Belcoda software running on a desktop computer"
			/>
		</div>
		<div
			class="lg:col-span-2 lg:col-start-1 lg:row-start-2 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8"
		>
			<div class="lg:pr-4">
				<div class="max-w-xl text-base/7 text-gray-700 lg:max-w-lg">
					<p>
						The Belcoda Foundation builds software for managing community groups and nonprofits,
						with a particular focus on low- and middle-income countries in the Global South.
					</p>
					<ul role="list" class="mt-8 space-y-8 text-gray-600">
						<li class="flex flex-nowrap items-start gap-x-3">
							<div><HeartHandshake size={24} class="mt-1" /></div>

							<div>
								<strong class="font-semibold text-gray-900">Built in partnership:</strong>
								We work directly with community leaders and social change advocates in low and middle-income
								countries at every step of development and delivery.
							</div>
						</li>
						<li class="flex flex-nowrap items-start gap-x-3">
							<div><ShieldCheck size={24} class="mt-1" /></div>
							<div>
								<strong class="font-semibold text-gray-900">Secure service delivery:</strong> We deliver
								software as a fully-managed hosted service with professional support and a focus on security,
								usability, accessibility and privacy.
							</div>
						</li>
						<li class="flex flex-nowrap items-start gap-x-3">
							<div><HandCoins size={24} class="mt-1" /></div>
							<div>
								<strong class="font-semibold text-gray-900">Free and open:</strong>
								We partner with civil society and philanthropic foundations to deliver all services free
								of charge to end users. Where possible, we also release our software under permissive
								open source licenses.
							</div>
						</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>

<style lang="postcss">
	.background-learning {
		background-image: url('/images/learning.webp');
	}

	/* .section-bg {
		background-image: url('/gradients/header_gradient4.svg');
		background-position: center;
		background-size: cover;
		background-repeat: no-repeat;
	} */
</style>
