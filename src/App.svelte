<script>
  import Designs from "./components/designs.svelte";
  import EducationSection from "./components/education-section.svelte";
  import MainSection from "./components/main-section.svelte";
  import Navbar from "./components/navbar.svelte";
  import ProjectSection from "./components/project-section.svelte";
  import WorkSection from "./components/work-section.svelte";
</script>

<div class=" min-h-screen bg-white relative">
  <div class="">
    <Navbar />
  </div>

  <div class="relative isolate px-6 pt-14 lg:px-8">
    <Designs />
    <div class="mx-auto max-w-2xl py-32 gap-10 flex flex-col sm:py-48 lg:py-56">
      <div class="min-h-screen">

      <MainSection />
</div>

      <div id="work">
        <WorkSection />
      </div>
      <div id="education">
        <EducationSection />
      </div>
      <div id="project">
        <ProjectSection />
      </div>
    </div>
  </div>
</div>
