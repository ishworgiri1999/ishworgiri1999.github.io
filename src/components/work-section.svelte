<script lang="ts">
  import Work from "./work.svelte";

  const works=[{role:'APpple',company:'elipzis gmbh',skills:['excel','react']}]
</script>

<div>
  <h3>Work</h3>

<ul role="list" class="divide-y divide-gray-100">

  {#each works as work}
  <Work {...work}/>
  {/each}

</ul>
</div>
