<script lang="ts">
	import Nav from '$lib/comps/Nav.svelte';
	import { type Snippet } from 'svelte';
	import { Component } from 'lucide-svelte';
	import {
		CalendarDays,
		Database,
		ClipboardPenLine,
		Mail,
		Globe,
		Users
	} from 'lucide-svelte/icons';
</script>

<svelte:head>
	<title>Software - Belcoda</title>
</svelte:head>

<Nav />
<section class="grid grid-cols-1 bg-gray-100 md:grid-cols-3 xl:grid-cols-6">
	<div class="none background-image bg-gray-300 md:block xl:col-span-3"></div>
	<div class="mx-8 py-24 sm:py-32 md:col-span-2 xl:col-span-3">
		<div class="lg:pr-4">
			<div class="lg:max-w-lg">
				<p class="text-base/7 font-semibold text-blue-600">Software</p>
				<h1
					class="mt-2 text-pretty text-4xl font-extrabold tracking-tight text-gray-900 sm:text-5xl"
				>
					The Belcoda Platform
				</h1>
				<p class="mt-6 text-xl/8 text-gray-700">
					The core Belcoda software is a flexible CRM supplemented by a range of modules that
					provide additional functionality.
				</p>

				<div class="mx-auto my-6 max-w-2xl sm:my-8 lg:my-12 lg:max-w-4xl">
					<dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-8 lg:max-w-none lg:gap-y-8">
						{@render detail(
							Database,
							'Community database',
							'A secure, centralized hub for managing all contact and membership details, ensuring information is always up-to-date.'
						)}
						{@render detail(
							Users,
							'Groups',
							'Organize members and volunteers into groups, integrate with existing WhatsApp groups and follow the conversation.'
						)}
						{@render detail(
							CalendarDays,
							'Events',
							'Build customizable event pages, send reminders via email or WhatsApp, track attendance, and more.'
						)}
						{@render detail(
							WhatsApp,
							'WhatsApp',
							'Leverage interactive templates, enable peer-to-peer messaging, and facilitate actions and signups through links or QR codes.'
						)}
						{@render detail(
							Mail,
							'Email',
							'Simplify email campaigns with list management, customizable templates, automated notifications, and newsletters.'
						)}
						{@render detail(
							ClipboardPenLine,
							'Petitions',
							'Create shareable petition pages with support for WhatsApp or web-based signatures, plus automated notifications.'
						)}
						{@render detail(
							Globe,
							'Website',
							'Easily create and update content with customizable templates, signup forms, custom subdomains, and more.'
						)}
					</dl>
				</div>

				<p class="mt-6 text-gray-700">
					For more information browse the <a
						href="https://github.com/belcoda/core"
						target="_blank"
						class="text-blue-600 underline">GitHub repository</a
					>
					or
					<a
						href="https://belcoda.notion.site/Documentation-835d2aed77ea4206ba97f6f71b962509"
						target="_blank"
						class="text-blue-600 underline">read the documentation</a
					>.
				</p>
			</div>
		</div>
	</div>
</section>

{#snippet detail(Fp: typeof Component | Snippet, title: string, text: string)}
	<div class="relative pl-16">
		<dt class="text-base/7 font-semibold text-gray-900">
			<div
				class="absolute left-0 top-0 mt-1.5 flex size-10 items-center justify-center rounded-lg bg-gradient-to-tr from-gray-900 to-slate-700"
			>
				<Fp class="text-white" />
			</div>
			{title}
		</dt>
		<dd class="mt-2 text-base/7 leading-normal text-gray-600">
			{text}
		</dd>
	</div>
{/snippet}

{#snippet WhatsApp()}
	<svg
		xmlns="http://www.w3.org/2000/svg"
		width="1em"
		height="1em"
		viewBox="0 0 24 24"
		{...$$props}
		class="m-1.5 h-auto w-full text-white"
		><path
			fill="currentColor"
			d="M19.05 4.91A9.82 9.82 0 0 0 12.04 2c-5.46 0-9.91 4.45-9.91 9.91c0 1.75.46 3.45 1.32 4.95L2.05 22l5.25-1.38c1.45.79 3.08 1.21 4.74 1.21c5.46 0 9.91-4.45 9.91-9.91c0-2.65-1.03-5.14-2.9-7.01m-7.01 15.24c-1.48 0-2.93-.4-4.2-1.15l-.3-.18l-3.12.82l.83-3.04l-.2-.31a8.26 8.26 0 0 1-1.26-4.38c0-4.54 3.7-8.24 8.24-8.24c2.2 0 4.27.86 5.82 2.42a8.18 8.18 0 0 1 2.41 5.83c.02 4.54-3.68 8.23-8.22 8.23m4.52-6.16c-.25-.12-1.47-.72-1.69-.81c-.23-.08-.39-.12-.56.12c-.17.25-.64.81-.78.97c-.14.17-.29.19-.54.06c-.25-.12-1.05-.39-1.99-1.23c-.74-.66-1.23-1.47-1.38-1.72c-.14-.25-.02-.38.11-.51c.11-.11.25-.29.37-.43s.17-.25.25-.41c.08-.17.04-.31-.02-.43s-.56-1.34-.76-1.84c-.2-.48-.41-.42-.56-.43h-.48c-.17 0-.43.06-.66.31c-.22.25-.86.85-.86 2.07s.89 2.4 1.01 2.56c.12.17 1.75 2.67 4.23 3.74c.59.26 1.05.41 1.41.52c.59.19 1.13.16 1.56.1c.48-.07 1.47-.6 1.67-1.18c.21-.58.21-1.07.14-1.18s-.22-.16-.47-.28"
		/></svg
	>
{/snippet}

<style lang="postcss">
	.background-image {
		background-image: url('/images/train.webp');
		background-position: center;
		background-size: cover;
	}
</style>
