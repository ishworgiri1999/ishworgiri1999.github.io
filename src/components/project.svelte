<script>
	export let name = '';
	export let description = '';
	export let technologies = [];
	export let link = '';
</script>

<li class="flex justify-between gap-x-6 py-6">
	<div class="flex gap-x-4">
		<div
			class="h-12 w-12 flex items-center justify-center rounded-full dark:bg-[#171717] bg-[#fafafa] dark:text-[#ededed] text-[#0a0a0a] font-medium"
		>
			<span>{name ? name[0].toUpperCase() : ''}</span>
		</div>
		<div class="min-w-0 flex-auto">
			<div class="flex gap-2 items-center">
				<a
					href={link}
					target="_blank"
					rel="noopener noreferrer"
					class="text-sm font-medium leading-6 dark:text-[#ededed] text-[#0a0a0a] hover:opacity-70 transition-opacity underline decoration-[#e5e5e5] dark:decoration-[#262626] underline-offset-4 inline-flex items-center gap-1"
				>
					{name}<svg class="inline-block h-3 w-3" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25" stroke-linecap="round" stroke-linejoin="round"></path></svg>
				</a>
			</div>

			<p class="mt-1 text-xs leading-5 dark:text-[#a3a3a3] text-[#525252]">
				{description}
			</p>
			{#if technologies.length > 0}
			<p class="mt-1 text-xs leading-5 dark:text-[#737373] text-[#737373]">
				{technologies.join(', ')}
			</p>
			{/if}
		</div>
	</div>
</li>
