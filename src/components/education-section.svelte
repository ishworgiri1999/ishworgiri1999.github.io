<script lang="ts">
 const educationData = [
  {
    school: "Technical University of Munich",
    major: "Masters in Computer Science",
    address: "Munich, Germany",
    duration: {
      start: "2022",
    },
  },
  {
    school: "Drexel University",
    address: "Philadelphia, USA",
    major: "Study Abroad - Computer Science",
    duration: {
      start: "2022",
      end: "2022",
    },
  },
  {
    school: "Jacobs University Bremen",
    major: "Bachelors in Computer Science",
    address: "Bremen, Germany",

    duration: {
      start: "2019",
      end: "2022",
    },
  },
];
  import Education from './education.svelte';
  </script>
  
  <div>
    <h3>Education</h3>
  <ul role="list" class="divide-y divide-gray-100">
  
    {#each educationData as ed}
    <Education {...ed}/>
    {/each}
  
  </ul>
</div>
