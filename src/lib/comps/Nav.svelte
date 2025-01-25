<script lang="ts">
	import { onClickOutside } from 'runed';
	import { fade, fly } from 'svelte/transition';
	let mobileNavOpen: boolean = $state(false);
	let { hideBackground }: { hideBackground?: boolean } = $props();
	let container = $state<HTMLElement>();
	onClickOutside(
		() => container,
		() => {
			mobileNavOpen = false;
		}
	);
</script>

<section>
	<nav
		class="fixed inset-x-0 top-0 z-10 px-4 py-3.5 transition-colors duration-300 ease-in-out lg:px-10"
		class:bg-gray-900={!hideBackground}
	>
		<div class="flex items-center justify-between">
			<a
				class="text-xl font-semibold text-white transition-opacity duration-300 ease-in-out"
				class:opacity-0={hideBackground}
				href="/"
			>
				<img src="/logos/white_logomark.svg" alt="Belcoda Foundation logo" class="h-7 w-auto" />
			</a>
			<button onclick={() => (mobileNavOpen = !mobileNavOpen)} class="text-white lg:hidden">
				<span class="sr-only">Open main menu</span>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="lucide lucide-menu"
					><line x1="4" x2="20" y1="12" y2="12" /><line x1="4" x2="20" y1="6" y2="6" /><line
						x1="4"
						x2="20"
						y1="18"
						y2="18"
					/></svg
				>
			</button>
			<div class="hidden lg:block">
				<a class="inline-block px-4 font-bold text-gray-100 hover:text-white" href="/about">About</a
				><a class="inline-block px-4 font-bold text-gray-100 hover:text-white" href="/software"
					>Software</a
				>
				<a class="inline-block px-4 font-bold text-gray-100 hover:text-white" href="/contact"
					>Contact</a
				>
			</div>
		</div>
	</nav>
	{#if mobileNavOpen}
		<div
			class="fixed bottom-0 left-0 top-0 z-50 w-5/6 max-w-sm bg-gray-900 bg-opacity-50"
			transition:fly={{ duration: 300, x: -100, y: 0 }}
		>
			<nav
				class="relative flex h-full w-full flex-col overflow-y-auto border-r bg-white py-8"
				bind:this={container}
			>
				<div class="mb-16 mt-12 flex justify-center pr-6">
					<a class="text-xl font-semibold leading-none text-gray-800" href="/">
						<img class="h-7" src="/logos/belcoda_dark.png" alt="" width="auto" />
					</a>
				</div>
				<div>
					<ul>
						<li class="mb-1">
							<a
								class="block rounded py-5 pl-16 font-semibold text-gray-800 hover:bg-gray-50"
								href="/about">About</a
							>
						</li>
						<li class="mb-1">
							<a
								class="block rounded py-5 pl-16 font-semibold text-gray-800 hover:bg-gray-50"
								href="/software">Software</a
							>
						</li>
						<li class="mb-1">
							<a
								class="block rounded py-5 pl-16 font-semibold text-gray-800 hover:bg-gray-50"
								href="/contact">Contact</a
							>
						</li>
					</ul>
				</div>
				<div class="mt-auto px-10">
					<p class="mb-4 mt-6 text-center text-xs text-gray-500">
						<span>© {new Date().getFullYear()} Belcoda Foundation. All rights reserved. </span>
					</p>
				</div>
			</nav>
		</div>
	{/if}
</section>
