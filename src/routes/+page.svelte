<script>
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

<div class="mx-auto max-w-2xl px-6 py-16 lg:py-24">
	<MainSection />

	<div id="work" class="mt-20">
		<WorkSection />
	</div>
	
	<div id="education" class="mt-20">
		<EducationSection />
	</div>
	
	<div id="project" class="mt-20">
		<ProjectSection />
	</div>

	<footer class="mt-20 pt-8 border-t border-[#e5e5e5] dark:border-[#262626]">
		<p class="text-xs dark:text-[#737373] text-[#737373]">
			© {new Date().getFullYear()} Ishwor Giri • Built with SvelteKit & TailwindCSS
		</p>
	</footer>
</div>
