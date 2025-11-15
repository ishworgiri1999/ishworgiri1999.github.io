<script lang="ts">
	import Project from './project.svelte';

	const projects = [
		{
			name: 'Quizel',
			link: 'https://github.com/ishworgiri1999/quizel',
			description:
				'This project is a simple quiz application fetching data from internet and presenting it as a game.',
			technologies: ['Dart', 'Flutter', 'Android/IOS']
		},
		{
			name: 'BlendEats',
			link: 'https://github.com/ishworgiri1999/BlendEats',

			description: 'Simple Food Marketplace made for diverse Community. Worked as a Team Member',
			technologies: ['PHP', 'MySQL', 'HTML/CSS']
		},
		{
			name: 'Beer Game',
			link: 'https://github.com/ishworgiri1999/se-03',
			description: 'A simple supply chain management system.',
			technologies: ['Python', 'REST API', 'Django']
		}
	];
</script>

<div>
	<h2 class="text-2xl font-semibold dark:text-[#ededed] text-[#0a0a0a] mb-8">Projects</h2>

	<ul role="list" class="divide-y divide-[#e5e5e5] dark:divide-[#262626]">
		{#each projects as project}
			<Project {...project} />
		{/each}
	</ul>
</div>
