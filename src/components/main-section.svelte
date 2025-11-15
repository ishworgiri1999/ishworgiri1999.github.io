<script>
	import { getContext } from 'svelte';

	const { darkMode, toggleDarkMode } = getContext('darkMode');
</script>

<div>
	<div class="mb-8 flex justify-between items-center">
		<img class="h-12 w-12" src="/logo.png" alt="Logo" />
		<button
			on:click={toggleDarkMode}
			type="button"
			class="p-2 hover:opacity-70 transition-opacity"
			aria-label="Toggle dark mode"
		>
			{#if $darkMode}
				<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
				</svg>
			{:else}
				<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" />
				</svg>
			{/if}
		</button>
	</div>

	<h1 class="text-4xl font-semibold tracking-tight dark:text-[#ededed] text-[#0a0a0a] mb-2">
		Ishwor Giri
	</h1>
	<p class="text-base dark:text-[#a3a3a3] text-[#525252] mb-12">
		Student, Software Developer, Tech Enthusiast
	</p>

	<div class="space-y-1 mb-12">
		<div class="flex items-center gap-2">
			<span class="text-sm dark:text-[#737373] text-[#737373] w-20">Github</span>
			<a
				href="https://github.com/ishworgiri1999"
				target="_blank"
				rel="noopener noreferrer"
				class="text-sm font-medium dark:text-[#ededed] text-[#0a0a0a] hover:opacity-70 transition-opacity underline decoration-[#e5e5e5] dark:decoration-[#262626] underline-offset-4 inline-flex items-center gap-1"
			>
				ishworgiri1999<svg class="inline-block h-3 w-3" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" stroke-linecap="round" stroke-linejoin="round"></path></svg>
			</a>
		</div>
		<div class="flex items-center gap-2">
			<span class="text-sm dark:text-[#737373] text-[#737373] w-20">Linkedin</span>
			<a
				href="https://www.linkedin.com/in/ishworgiri1999/"
				target="_blank"
				rel="noopener noreferrer"
				class="text-sm font-medium dark:text-[#ededed] text-[#0a0a0a] hover:opacity-70 transition-opacity underline decoration-[#e5e5e5] dark:decoration-[#262626] underline-offset-4 inline-flex items-center gap-1"
			>
				ishworgiri1999<svg class="inline-block h-3 w-3" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" stroke-linecap="round" stroke-linejoin="round"></path></svg>
			</a>
		</div>
		<div class="flex items-center gap-2">
			<span class="text-sm dark:text-[#737373] text-[#737373] w-20">Email</span>
			<a
				href="mailto:hi@ishworgiri.com.np"
				class="text-sm font-medium dark:text-[#ededed] text-[#0a0a0a] hover:opacity-70 transition-opacity underline decoration-[#e5e5e5] dark:decoration-[#262626] underline-offset-4 inline-flex items-center gap-1"
			>
				hi@ishworgiri.com.np<svg class="inline-block h-3 w-3" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" stroke-linecap="round" stroke-linejoin="round"></path></svg>
			</a>
		</div>
	</div>

	<div class="mb-12">
		<h2 class="text-2xl font-semibold dark:text-[#ededed] text-[#0a0a0a] mb-4">About me</h2>
		<p class="text-lg leading-relaxed dark:text-[#a3a3a3] text-[#525252]">
			I specialize in full stack development and have a strong interest in computer networks, security, and cloud computing. Currently pursuing my studies while working on impactful software projects.
		</p>
	</div>
</div>
