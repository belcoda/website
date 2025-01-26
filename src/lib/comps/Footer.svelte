<script lang="ts">
	const { call_url }: { call_url: string } = $props();
</script>

<section class="relative overflow-hidden bg-gray-900 pt-24">
	<img
		class="absolute bottom-0 left-1/2 h-full -translate-x-1/2 transform"
		src="/gradients/footer_bg_gradient.svg"
		alt=""
	/>
	<div class="container relative z-10 mx-auto px-4">
		<div class="border-b border-gray-700 pb-24">
			<div class="-m-8 flex flex-wrap">
				<div class="w-full p-8 sm:w-1/2 lg:w-6/12">
					<div class="lg:max-w-sm">
						<a class="mb-8 inline-block" href="/">
							<img src="/logos/belcoda_white.png" alt="Belcoda logo" class="h-12" />
						</a>
						<div class="-m-1.5 flex flex-wrap">
							<div class="w-auto p-1.5">
								<a
									href="https://github.com/belcoda/core"
									target="_blank"
									aria-label="Link to GitHub repository"
								>
									<div
										class="flex h-9 w-9 items-center justify-center rounded-full border border-gray-800 text-gray-300 hover:border-gray-900 hover:text-gray-100"
									>
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
											class="lucide lucide-github"
											><path
												d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"
											></path><path d="M9 18c-4.51 2-5-2-7-2"></path></svg
										>
									</div>
								</a>
							</div>
							<div class="w-auto p-1.5">
								<a
									href="https://discord.gg/q7xPnzvswy"
									target="_blank"
									aria-label="Join us on Discord"
								>
									<div
										class="flex h-9 w-9 items-center justify-center rounded-full border border-gray-800 text-gray-300 hover:border-gray-900 hover:text-gray-100"
									>
										<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
											><path
												d="M8.52062 13.8458C7.48059 13.8458 6.63159 12.9014 6.63159 11.7446 6.63159 10.5879 7.45936 9.64331 8.52062 9.64331 9.57123 9.64331 10.4308 10.5879 10.4096 11.7446 10.4096 12.9014 9.57123 13.8458 8.52062 13.8458ZM15.4941 13.8458C14.454 13.8458 13.604 12.9014 13.604 11.7446 13.604 10.5879 14.4328 9.64331 15.4941 9.64331 16.5447 9.64331 17.4043 10.5879 17.3831 11.7446 17.3831 12.9014 16.5553 13.8458 15.4941 13.8458ZM10.1253 4.32296 9.81655 3.76001 9.18323 3.86556C7.71915 4.10958 6.32658 4.54677 5.02544 5.14604L4.79651 5.25148 4.65507 5.46009C2.0418 9.31441 1.3258 13.1087 1.68032 16.8362L1.71897 17.2425 2.04912 17.4824C3.78851 18.7465 5.47417 19.5189 7.12727 20.0257L7.91657 20.2676 9.03013 17.5506C10.9397 18.0226 13.0592 18.0228 14.969 17.5511L16.0757 20.2683 16.8668 20.0256C18.5173 19.5193 20.2137 18.7472 21.9466 17.4811L22.2726 17.243 22.3131 16.8414C22.7491 12.5213 21.616 8.75773 19.3547 5.45652L19.2128 5.24944 18.9846 5.14504C17.6767 4.54685 16.2852 4.10981 14.8309 3.86573L14.2132 3.76207 13.8987 4.30369C13.8112 4.45445 13.7215 4.62464 13.6364 4.79687 12.5441 4.6847 11.456 4.68446 10.3726 4.79652 10.2882 4.62736 10.2025 4.4638 10.1253 4.32296ZM6.71436 16.6102C6.91235 16.7243 7.11973 16.8358 7.32557 16.9381L6.8764 18.034C5.75585 17.6259 4.61837 17.0637 3.4476 16.2557 3.22313 13.1178 3.86092 9.951 6.01196 6.68626 6.90962 6.29123 7.8535 5.98279 8.83606 5.77295 8.89631 5.89831 8.95235 6.02066 8.99839 6.12917L9.27128 6.77238 9.96259 6.67098C11.3152 6.4726 12.6772 6.47234 14.0523 6.67124L14.7424 6.77106 15.0147 6.12917C15.0621 6.01743 15.1167 5.89547 15.1743 5.77322 16.1525 5.98326 17.098 6.29212 18.0029 6.68812 19.8781 9.50857 20.8241 12.6544 20.5486 16.2552 19.3837 17.0625 18.2422 17.6249 17.1193 18.0335L16.6735 16.939C16.8799 16.8365 17.0879 16.7246 17.2865 16.6102 17.7763 16.328 18.3039 15.976 18.6402 15.6397L17.3606 14.3602C17.1969 14.5239 16.837 14.7808 16.3831 15.0423 15.9388 15.2983 15.498 15.5052 15.2164 15.5983 13.2126 16.2608 10.7883 16.2608 8.78443 15.5983 8.50285 15.5052 8.06205 15.2983 7.61772 15.0423 7.16383 14.7808 6.80392 14.5239 6.64017 14.3602L5.36065 15.6397C5.6969 15.976 6.2245 16.328 6.71436 16.6102Z"
											></path></svg
										>
									</div>
								</a>
							</div>
						</div>
					</div>
				</div>
				<div class="w-full p-8 sm:w-1/2 lg:w-2/12">
					<h3 class="tracking-px mb-8 text-sm font-semibold uppercase leading-normal text-gray-600">
						Software
					</h3>
					<ul>
						<li class="mb-5">
							<a class="font-medium leading-relaxed text-white hover:text-gray-200" href="/software"
								>Features</a
							>
						</li>
						<li class="mb-5">
							<a
								class="font-medium leading-relaxed text-white hover:text-gray-200"
								href="https://belcoda.notion.site/Documentation-835d2aed77ea4206ba97f6f71b962509?pvs=74"
								target="_blank">Documentation</a
							>
						</li>
						<li>
							<a
								class="font-medium leading-relaxed text-white hover:text-gray-200"
								href="https://belcoda.notion.site/Roadmap-098edea17a19414d9f201ae607397218?pvs=4"
								target="_blank">Roadmap</a
							>
						</li>
					</ul>
				</div>

				<div class="w-full p-8 sm:w-1/2 lg:w-2/12">
					<h3 class="tracking-px mb-8 text-sm font-semibold uppercase leading-normal text-gray-600">
						Foundation
					</h3>
					<ul>
						<li class="mb-5">
							<a class="font-medium leading-relaxed text-white hover:text-gray-200" href="/about"
								>About</a
							>
						</li>
						<li class="mb-5">
							<a class="font-medium leading-relaxed text-white hover:text-gray-200" href="/contact"
								>Contact</a
							>
						</li>
						<li class="mb-5">
							<a
								class="font-medium leading-relaxed text-white hover:text-gray-200"
								href="https://belcoda.notion.site/Jobs-78f34ed4508d46f69a92e5fea15a7e19"
								target="_blank">Careers</a
							>
						</li>
						<li class="mb-5">
							<a
								class="font-medium leading-relaxed text-white hover:text-gray-200"
								href={call_url}
								target="_blank">Book a call</a
							>
						</li>
					</ul>
				</div>
				<div class="w-full p-8 sm:w-1/2 lg:w-2/12">
					<h3 class="tracking-px mb-8 text-sm font-semibold uppercase leading-normal text-gray-600">
						Information
					</h3>
					<ul>
						<li class="mb-5">
							<a
								class="font-medium leading-relaxed text-white hover:text-gray-200"
								href="https://discord.gg/q7xPnzvswy"
								target="_blank">Discord</a
							>
						</li>
						<li class="mb-5">
							<a
								class="font-medium leading-relaxed text-white hover:text-gray-200"
								href="https://github.com/belcoda/belcoda/blob/main/LICENSE"
								target="_blank">License</a
							>
						</li>
						<li class="mb-5">
							<a
								class="font-medium leading-relaxed text-white hover:text-gray-200"
								href="https://github.com/belcoda/belcoda/blob/main/CONTRIBUTING.md"
								target="_blank">Contributor Guidelines</a
							>
						</li>
						<li>
							<a class="font-medium leading-relaxed text-white hover:text-gray-200" href="/privacy"
								>Privacy Policy</a
							>
						</li>
					</ul>
				</div>
			</div>
		</div>
		<p class="py-5 text-center text-sm font-medium leading-normal text-gray-300">
			Copyright © {new Date().getFullYear()} Belcoda Foundation, Inc. All Rights Reserved
		</p>
		<p
			class="mx-auto mb-12 max-w-4xl px-8 text-center text-xs font-light leading-normal text-gray-400"
		>
			The Belcoda Foundation is in the process of obtaining 501(c)(3) status from the Internal
			Revenue Service. IRS Pub 557 indicates that the effective date of our exemption will be
			retroactive to our date of incorporation. Donations may be tax exempt.
		</p>
	</div>
</section>
