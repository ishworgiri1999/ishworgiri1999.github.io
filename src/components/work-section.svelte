<script lang="ts">
	import Work from './work.svelte';

	const works = [
		{
			role: 'Software Developer',
			company: 'fruits GmbH',
			address: 'Munich, Germany',
			skills: ['Next.js', 'React', 'Go', 'Terraform'],
			duration: { start: 'July 2025' }
		},
		{
			role: 'Software Developer - Working Student',
			company: 'fruits GmbH',
			address: 'Munich, Germany',
			skills: ['Next.js', 'React', 'Go', 'Terraform'],
			duration: { start: 'April 2023', end: 'June 2025' }
		},
		{
			role: 'Software Developer - Working Student',
			address: 'Bremen, Germany',
			company: 'elipzis GmbH',
			skills: ['React Native', 'React', 'Svelte'],
			duration: { start: 'April 2021', end: 'March 2023' }
		}
	];

	// Group works by company
	const groupedWorks = works.reduce((acc, work) => {
		const key = work.company;
		if (!acc[key]) {
			acc[key] = {
				company: work.company,
				address: work.address,
				roles: []
			};
		}
		acc[key].roles.push({
			role: work.role,
			skills: work.skills,
			duration: work.duration
		});
		return acc;
	}, {} as Record<string, { company: string; address: string; roles: Array<{ role: string; skills: string[]; duration: { start: string; end?: string } }> }>);

	const groupedWorksArray = Object.values(groupedWorks);
</script>

<div>
	<h2 class="text-2xl font-semibold dark:text-[#ededed] text-[#0a0a0a] mb-8">Work</h2>

	<ul role="list" class="divide-y divide-[#e5e5e5] dark:divide-[#262626]">
		{#each groupedWorksArray as group}
			<Work company={group.company} address={group.address} roles={group.roles} />
		{/each}
	</ul>
</div>
