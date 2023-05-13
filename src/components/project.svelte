<script>
  export let name = "";
  export let description = "";
  export let technologies = [];
  export let link = "";
</script>

<li class="flex justify-between gap-x-6 py-5">
  <div class="flex gap-x-4">
    <div
      class="h-12 w-12 flex items-center justify-center rounded-full bg-gray-50"
    >
      <span>{name ? name[0].toUpperCase() : ""}</span>
    </div>
    <div class="min-w-0 flex-auto">
      <p class="text-sm font-semibold leading-6 text-gray-900">
        {name}
      </p>
      <p class="mt-1 truncate text-xs leading-5 text-gray-500">
        {description}
      </p>
      <ul class="flex gap-2 mt-1 text-sm">
        {#each technologies as t}
          <li class="border-gray-100 px-1 border rounded-md">{t}</li>
        {/each}
      </ul>
    </div>
  </div>
  <div class="w-max">
    <a href={link} class="px-1 border-2 rounded-full border border-purple-500 text-m leading-5 text-purple-500">
      → 
    </a>
  </div>
</li>
