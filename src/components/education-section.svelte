<script lang="ts">
	const educationData = [
		{
			school: 'Technical University of Munich',
			major: 'Masters in Computer Science',
			address: 'Munich, Germany',
			duration: {
				start: ' October 2022'
			}
		},
		{
			school: 'Drexel University',
			address: 'Philadelphia, USA',
			major: 'Study Abroad - Computer Science',
			duration: {
				start: 'September 2021',
				end: 'December 2021'
			}
		},
		{
			school: 'Jacobs University Bremen',
			major: 'Bachelors in Computer Science',
			address: 'Bremen, Germany',

			duration: {
				start: 'August 2019',
				end: 'June 2022'
			}
		}
	] as const;
	import Education from './education.svelte';
</script>

<div>
	<h3 class="text-2xl">Education</h3>
	<ul role="list" class="divide-y divide-gray-100">
		{#each educationData as ed}
			<Education {...ed} />
		{/each}
	</ul>
</div>
