<script lang="ts">
	import Nav from '$lib/comps/Nav.svelte';
</script>

<Nav />
<svelte:head>
	<title>Contact - Belcoda</title>
</svelte:head>
<section class="isolate bg-gray-100 px-6 py-24 sm:py-32 lg:px-8 lg:pb-32 lg:pt-40">
	<div class="mx-auto max-w-2xl text-center">
		<h2 class="text-balance text-4xl font-extrabold tracking-tight text-gray-800 sm:text-5xl">
			Contact us
		</h2>
		<p class="mt-2 text-lg/8 text-gray-600">
			Get in touch with us to discuss potential partnership opportunities, or with any questions or
			requests.
		</p>
	</div>
	<form
		method="POST"
		class="mx-auto mt-6 max-w-xl sm:mt-8"
		action="/contact/success"
		data-netlify-honeypot="bot-field"
		data-netlify="true"
	>
		<!-- <input type="hidden" name="form-name" value="belcoda-homepage-contact" /> -->
		<div class="grid grid-cols-1 gap-x-8 gap-y-6 sm:grid-cols-2">
			<div class="sm:col-span-2">
				<label for="name" class="block text-sm/6 font-semibold text-gray-700">Name</label>
				<div class="mt-2.5">
					<input
						type="text"
						name="name"
						id="name"
						autocomplete="name"
						class="block w-full rounded-md border-gray-400 bg-gray-100 px-3.5 py-2 text-sm text-gray-900 outline-1 -outline-offset-1 outline-gray-300 placeholder:text-gray-400 focus:outline-2 focus:-outline-offset-2 focus:outline-blue-600"
					/>
				</div>
			</div>
			<div class="sm:col-span-2">
				<label for="company" class="block text-sm/6 font-semibold text-gray-700"
					>Company/organization</label
				>
				<div class="mt-2.5">
					<input
						type="text"
						name="company"
						id="company"
						autocomplete="organization"
						class="block w-full rounded-md border-gray-400 bg-gray-100 px-3.5 py-2 text-sm text-gray-900 outline-1 -outline-offset-1 outline-gray-300 placeholder:text-gray-400 focus:outline-2 focus:-outline-offset-2 focus:outline-blue-600"
					/>
				</div>
			</div>
			<div class="sm:col-span-2">
				<label for="email" class="block text-sm/6 font-semibold text-gray-700">Email</label>
				<div class="mt-2.5">
					<input
						type="email"
						name="email"
						id="email"
						autocomplete="email"
						class="block w-full rounded-md border-gray-400 bg-gray-100 px-3.5 py-2 text-sm text-gray-900 outline-1 -outline-offset-1 outline-gray-300 placeholder:text-gray-400 focus:outline-2 focus:-outline-offset-2 focus:outline-blue-600"
					/>
				</div>
			</div>

			<div class="sm:col-span-2">
				<label for="message" class="block text-sm/6 font-semibold text-gray-700">Message</label>
				<div class="mt-2.5">
					<textarea
						name="message"
						id="message"
						rows="4"
						class="block w-full rounded-md border-gray-400 bg-gray-100 px-3.5 py-2 text-sm text-gray-900 outline-1 -outline-offset-1 outline-gray-300 placeholder:text-gray-400 focus:outline-2 focus:-outline-offset-2 focus:outline-blue-600"
					></textarea>
				</div>
			</div>
		</div>
		<div class="mt-10">
			<button
				type="submit"
				class="shadow-xs block w-full rounded-md bg-gray-800 px-3.5 py-2.5 text-center text-sm font-semibold text-white hover:bg-gray-700 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
				>Contact</button
			>
		</div>
	</form>
</section>
