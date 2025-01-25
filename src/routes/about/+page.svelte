<script lang="ts">
	import Nav from '$lib/comps/Nav.svelte';
	import GlobeLock from 'lucide-svelte/icons/globe-lock';
	import HandHeart from 'lucide-svelte/icons/hand-heart';
	import MessagesSquare from 'lucide-svelte/icons/messages-square';
	import Smartphone from 'lucide-svelte/icons/smartphone';
</script>

<Nav />
<svelte:head>
	<title>About - Belcoda</title>
</svelte:head>
<section class="grid grid-cols-1 bg-gray-100 md:grid-cols-3 xl:grid-cols-6">
	<div class="none background-image bg-gray-300 md:block xl:col-span-3"></div>
	<div class="mx-8 py-24 sm:py-32 md:col-span-2 xl:col-span-3">
		<div class="lg:pr-4">
			<div class="lg:max-w-lg">
				<p class="text-base/7 font-semibold text-blue-600">About us</p>
				<h1
					class="mt-2 text-pretty text-4xl font-extrabold tracking-tight text-gray-900 sm:text-5xl"
				>
					The Belcoda Foundation
				</h1>
				<p class="mt-6 text-xl/8 text-gray-700">
					Community leaders create change by building connections between people. And the internet
					has revolutionized how we connect.
				</p>
				<p class="mt-4 text-gray-700">
					Technology has the power to supercharge social change. But many community leaders,
					especially those working outside the United States and other rich countries, don't have
					access to the software they need to grow and scale their impact.
				</p>

				<p class="mt-4 text-gray-700">
					The Belcoda Foundation was created to change that. We build software focused on the
					specific needs of locally-led nonprofits and grassroots community initiatives in low- and
					middle-income countries.
				</p>
				<ul
					role="list"
					class="mt-6 grid grid-cols-1 items-baseline gap-6 text-gray-600 md:grid-cols-2"
				>
					<li class="flex flex-nowrap items-start gap-x-3">
						<div><GlobeLock size={16} class="mt-2" /></div>

						<div>
							<strong class="font-semibold text-gray-800">The places people live:</strong>
							Our software supports multiple languages, currencies, time zones, address formats and more.
						</div>
					</li>
					<li class="flex flex-nowrap items-start gap-x-3">
						<div><MessagesSquare size={16} class="mt-2" /></div>

						<div>
							<strong class="font-semibold text-gray-800">The ways people connect:</strong>
							We deliver first-class support for popular messaging channels like WhatsApp.
						</div>
					</li>
					<li class="flex flex-nowrap items-start gap-x-3">
						<div><Smartphone size={16} class="mt-2" /></div>

						<div>
							<strong class="font-semibold text-gray-800">The devices people use:</strong>
							Even our most advanced tools can be used on a basic smartphone with low bandwidth and limited
							data.
						</div>
					</li>
					<li class="flex flex-nowrap items-start gap-x-3">
						<div><HandHeart size={16} class="mt-2" /></div>

						<div>
							<strong class="font-semibold text-gray-800">The support people need:</strong>
							Free hands-on training and support – and access to a global network of software-enabled
							community leaders.
						</div>
					</li>
				</ul>

				<p class="mt-6 text-gray-700">
					The Belcoda Foundation works with philanthropic foundations and civil society to deliver
					software that is free, open, and built in partnership with the people who use it.
				</p>
			</div>
		</div>
	</div>
</section>

<style lang="postcss">
	.background-image {
		background-image: url('/images/image_about.jpg');
		background-position: center;
		background-size: cover;
	}
</style>
