<script>
	import Designs from '../components/designs.svelte';
	import EducationSection from '../components/education-section.svelte';
	import MainSection from '../components/main-section.svelte';
	import ProjectSection from '../components/project-section.svelte';
	import WorkSection from '../components/work-section.svelte';
</script>

<svelte:head>
	<title>Ishwor Giri</title>
	<meta
		name="description"
		content="Ishwor Giri - Student, Tech Enthusiast, Software Developer - Portfolio"
	/>
</svelte:head>

<div class="relative isolate">
	<Designs />
	<div class="mx-auto max-w-2xl py-12 gap-16 flex flex-col">
		<div class="relative">
			<MainSection />
		</div>

		<div id="work" class="relative">
			<WorkSection />
		</div>
		<div id="education">
			<EducationSection />
		</div>
		<div id="project">
			<ProjectSection />
		</div>

		<div class="relative text-center">
			<Designs />

			<div>
				<a
					href="/cv.pdf"
					class="rounded-md border border-purple-300 px-1 text-purple-500 text-sm font-semibold shadow-sm"
					>Download My CV</a
				>
			</div>
		</div>
	</div>
</div>
