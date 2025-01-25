<script lang="ts">
	import Nav from '$lib/comps/Nav.svelte';
	import Heading_2 from 'lucide-svelte/icons/heading-2';
</script>

<svelte:head>
	<title>Privacy - Belcoda</title>
</svelte:head>
<Nav />
<section class="section-bg bg-white py-24 sm:py-32">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-2xl">
			<h2 class="text-base/7 font-semibold text-indigo-600">Privacy Policy</h2>
			<p
				class="mt-2 text-pretty text-4xl font-extrabold tracking-tight text-gray-900 sm:text-5xl lg:text-balance"
			>
				The Belcoda Foundation takes privacy very seriously.
			</p>
			<p class="mt-6 text-lg/8 text-gray-600">
				To better protect your privacy we provide this privacy policy notice explaining the way your
				personal information is collected and used.
			</p>
			<div class="text-gray-600">
				{@render heading2('Collection of Routine Information')}

				<p>
					The Belcoda application, this website, and other Belcoda products track basic information
					about their visitors and users. This information includes, but is not limited to, IP
					addresses, browser details, timestamps and referring pages. None of this information can
					personally identify specific visitors or users. The information is tracked for routine
					administration and maintenance purposes.
				</p>

				{@render heading2('Collection of Personal Information')}

				<p>
					As part of the necessary operations of Belcoda products, this website, and the Belcoda
					application, certain personal information is collected. This information includes, but is
					not limited to, email addresses, phone numbers, and names. This information is used to
					create user accounts, send notifications, and provide customer support. This information
					is stored securely and is not shared with third parties.
				</p>

				<p class="mt-3">
					Self hosted instances of the Belcoda application do not transmit personal information to
					Belcoda LLC. The personal information collected via self hosted instances of the Belcoda
					application is stored on the instance manager's infrastructure and is not accessible by
					Belcoda LLC.
				</p>

				<p class="mt-3">
					Depending on its configuration settings, a self-hosted Belcoda instance may transmit
					routine information to Belcoda LLC. This information includes, but is not limited to, IP
					addresses, browser details, timestamps and referring pages. None of this information can
					personally identify specific visitors or users. The information is tracked for routine
					administration and maintenance purposes.
				</p>

				{@render heading2('Cookies')}
				<p>
					Where necessary, this website, and other Belcoda products, use cookies to store
					information about a visitor’s preferences and history in order to better serve the vistor
					or user and/or present the visitor or user with customized content.
				</p>

				{@render heading2('Advertisement and Other Third Parties')}
				<p>
					Belcoda does not user advertising or third party trackers, and does not share any user
					information with third parties, other than for the purposes of administering the Belcoda
					application and related products.
				</p>

				{@render heading2('Links to Third Party Websites')}
				<p>
					We have included links on this website, and in other Belcoda products, for your use and
					reference. We are not responsible for the privacy policies on these websites. You should
					be aware that the privacy policies of these websites may differ from our own.
				</p>

				{@render heading2('Security')}
				<p>
					The security of your personal information is important to us, but remember that no method
					of transmission over the Internet, or method of electronic storage, is 100% secure. While
					we aim to follow industry best practices in relation to security and protection of
					personal information and user data, we cannot guarantee its absolute security.
				</p>

				{@render heading2('Changes To This Privacy Policy')}
				<p>
					This Privacy Policy is effective as of 6 June 2024 and will remain in effect except with
					respect to any changes in its provisions in the future, which will be in effect
					immediately after being posted on this page.
				</p>

				<p class="mt-3">
					We reserve the right to update or change our Privacy Policy at any time and you should
					check this Privacy Policy periodically. If we make any material changes to this Privacy
					Policy, we will notify you either through the email address you have provided us, or by
					placing a prominent notice on our website.
				</p>

				{@render heading2('Contact Information')}
				<p>
					For any questions or concerns regarding the privacy policy, please <a
						class="text-blue-600 underline"
						href="/contact">contact us</a
					>.
				</p>
			</div>
		</div>
	</div>
</section>

{#snippet heading2(text: string)}
	<h2 class="mb-3 mt-6 text-2xl font-bold tracking-tight text-gray-900">{text}</h2>
{/snippet}
