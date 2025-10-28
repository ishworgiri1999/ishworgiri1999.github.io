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
	] as const;
</script>

<div>
	<h3 class="text-2xl">Projects</h3>

	<ul role="list" class="divide-y divide-gray-100">
		{#each projects as project}
			<Project {...project} />
		{/each}
	</ul>
</div>
