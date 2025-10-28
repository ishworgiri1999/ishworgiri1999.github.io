<script lang="ts">
	import Chip from './chip.svelte';
	export let name = '';
	export let description = '';
	export let technologies: readonly string[] = [];
	export let link = '';
</script>

<li class="flex justify-between gap-x-6 py-5">
	<div class="flex gap-x-4">
		<div
			class="h-12 w-12 flex items-center justify-center rounded-full dark:bg-gray-900 bg-gray-50"
		>
			<span>{name ? name[0].toUpperCase() : ''}</span>
		</div>
		<div class="min-w-0 flex-auto">
			<div class="flex gap-2 items-center">
				<p class=" text-sm font-semibold leading-6 dark:text-gray-100 text-gray-900">
					{name}
				</p>
				<div class="w-max">
					<a
						href={link}
						class="text-xs px-1 rounded-full border border-purple-500 dark:border-purple-300 dark:text-purple-300 text-purple-500"
					>
						→
					</a>
				</div>
			</div>

			<p class="mt-1 text-xs leading-5 dark:text-gray-50 text-gray-500">
				{description}
			</p>
			<ul class="flex gap-2 mt-1 text-sm">
				{#each technologies as t}
					<Chip>{t}</Chip>
				{/each}
			</ul>
		</div>
	</div>
</li>
