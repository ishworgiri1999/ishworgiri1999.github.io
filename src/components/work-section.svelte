<script lang="ts">
	import Work from './work.svelte';

	const works = [
    {
			role: 'Software Developer - Working Student',
			company: 'fruits GmbH',
      address:"Munich, Germany",
			skills: ['next.js', 'react'],
			duration: { start: 'April 2023'}
		},
		{
			role: 'Software Developer - Working Student',
      address:"Bremen, Germany",
			company: 'elipzis GmbH',
			skills: ['react native', 'react'],
			duration: { start: 'April 2021',end:'March 2023' }
		}
	];
</script>

<div>
	<h3>Work</h3>

	<ul role="list" class="divide-y divide-gray-100">
		{#each works as work}
			<Work {...work} />
		{/each}
	</ul>
</div>
