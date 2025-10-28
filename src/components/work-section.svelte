<script lang="ts">
	import Work from './work.svelte';

	const works = [
		{
			role: 'Software Developer - Working Student',
			company: 'fruits GmbH',
			address: 'Munich, Germany',
			skills: ['Next.js', 'React', 'Go', 'Terrafom'],
			duration: { start: 'April 2023' }
		},
		{
			role: 'Software Developer - Working Student',
			address: 'Bremen, Germany',
			company: 'elipzis GmbH',
			skills: ['React Native', 'React', 'Svelte'],
			duration: { start: 'April 2021', end: 'March 2023' }
		}
	] as const;
</script>

<div>
	<h3 class="text-2xl">Work</h3>

	<ul role="list" class="divide-y divide-gray-100">
		{#each works as work}
			<Work {...work} />
		{/each}
	</ul>
</div>
