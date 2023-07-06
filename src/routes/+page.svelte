<script>
	import Designs from '../components/designs.svelte';
	import EducationSection from '../components/education-section.svelte';
	import MainSection from '../components/main-section.svelte';
	import ProjectSection from '../components/project-section.svelte';
	import WorkSection from '../components/work-section.svelte';
</script>


<svelte:head>
  <title>Ishwor Giri</title>
  <meta name="description" content="Ishwor Giri - Student, Tech Enthusiast, Software Developer - Portfolio" />
</svelte:head>


<div class="relative isolate">
	<Designs />
	<div class="mx-auto max-w-2xl py-32 gap-16 flex flex-col sm:py-48 lg:py-56">
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
			class="rounded-md bg-green-500 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm "
			>Download My CV</a
		  >
		  </div>
		  <div class="mt-10">
		  <span class='text-xs text-gray-400'>*  Website under construction</span>
		</div>
		</div>
	</div>
</div>
