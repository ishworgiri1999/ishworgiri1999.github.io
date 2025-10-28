<script lang="ts">
	let showDialog = false;

	const navs = [
		{ title: 'Work', href: '#work' },
		{ title: 'Education', href: '#education' },
		{ title: 'Projects', href: '#project' }
	] as const;
</script>

<header class="absolute inset-x-0 top-0 z-50">
	<nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
		<div class="flex">
			<a href="/" class="-m-1.5 p-1.5">
				<span class="sr-only">Your Company</span>
				<img class="h-12 w-auto" src="/logo.png" alt="" />
			</a>
		</div>

		<div class="hidden lg:flex lg:gap-x-12">
			{#each navs as nav}
				<a href={nav.href} class="text-sm font-semibold leading-6 dark:text-gray-100 text-gray-900"
					>{nav.title}</a
				>
			{/each}
		</div>
		<div class="flex lg:invisible">
			<button
				on:click={() => (showDialog = true)}
				type="button"
				class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 dark:text-gray-50 text-gray-700"
			>
				<span class="sr-only">Open main menu</span>
				<svg
					class="h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					aria-hidden="true"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
					/>
				</svg>
			</button>
		</div>
	</nav>
	<!-- Mobile menu, show/hide based on menu open state. -->
	<div class="{showDialog ? '' : 'hidden'} lg:hidden" role="dialog" aria-modal="true">
		<!-- Background backdrop, show/hide based on slide-over state. -->
		<div class="fixed inset-0 z-50" />
		<div
			class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto dark:bg-slate-800 bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
		>
			<div class="flex items-center justify-between">
				<a href="/" class="-m-1.5 p-1.5">
					<span class="sr-only">Ishwor Giri</span>
					<img class="h-12 w-auto" src="/logo.png" alt="" />
				</a>
				<button
					on:click={() => (showDialog = false)}
					type="button"
					class="-m-2.5 rounded-md p-2.5 dark:text-gray-50 text-gray-700"
				>
					<span class="sr-only">Close menu</span>
					<svg
						class="h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
				</button>
			</div>
			<div class="mt-6 flow-root">
				<div class="-my-6 divide-y divide-gray-500/10">
					<div class="space-y-2 py-6">
						{#each navs as nav}
							<a
								href={nav.href}
								class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 dark:text-gray-50 text-gray-900
                  dark:hover:text-gray-900
                  hover:bg-gray-50">{nav.title}</a
							>
						{/each}
					</div>
				</div>
			</div>
		</div>
	</div>
</header>
