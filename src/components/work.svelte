<script lang="ts">
	import Chip from './chip.svelte';

	export let role = '';
	export let company = '';
	export let address = '';
	export let skills: readonly string[] = [];
	export let duration: { start: string; end?: string } = { start: '' };
</script>

<li class="flex justify-between gap-x-6 py-5">
	<div class="flex gap-x-4">
		<div
			class="h-12 w-12 flex items-center justify-center rounded-full dark:bg-gray-900 bg-gray-50"
		>
			<span>{company ? company[0].toUpperCase() : ''}</span>
		</div>
		<div class="min-w-0 flex-auto">
			<p class="text-sm font-semibold leading-6 dark:text-gray-100 text-gray-700">
				{role}
			</p>
			<p class="mt-1 truncate text-xs leading-5 dark:text-gray-300 text-gray-500">
				{company}
			</p>
			<ul class="flex gap-2 mt-1 text-sm">
				{#each skills as t}
					<Chip>{t}</Chip>
				{/each}
			</ul>
		</div>
	</div>
	<div class="sm:flex sm:flex-col sm:items-end">
		<p class="text-sm leading-6 dark:text-gray-300 text-gray-900">{address}</p>
		<p class="mt-1 text-xs leading-5 dark:text-gray-200 text-gray-500">
			<span>{duration.start} - {duration.end ?? 'present'}</span>
		</p>
	</div>
</li>
