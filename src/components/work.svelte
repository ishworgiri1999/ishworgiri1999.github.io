<script>
    export let company=''
    export let address =''
    export let roles = []
    export let imageUrl=''
</script>

<li class="flex gap-x-6 py-6">
    <div class="flex gap-x-4 flex-shrink-0">
      {#if imageUrl}
      <img
        class="h-12 w-12 flex-none rounded-full dark:bg-[#171717] bg-[#fafafa]"
        src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
        alt=""
      />
      {:else}
      <div
      class="h-12 w-12 flex items-center justify-center rounded-full dark:bg-[#171717] bg-[#fafafa] dark:text-[#ededed] text-[#0a0a0a] font-medium"
    ><span>{company?company[0].toUpperCase():''}</span></div>
      {/if}
    </div>
    <div class="flex-1 min-w-0">
      <div class="flex justify-between items-start mb-2">
        <p class="text-xs leading-5 dark:text-[#a3a3a3] text-[#525252]">
          {company}
        </p>
        <p class="text-sm leading-6 dark:text-[#a3a3a3] text-[#525252]">{address}</p>
      </div>
      {#each roles as roleItem, i}
        <div class="{i > 0 ? 'mt-3' : ''}">
          <div class="flex justify-between items-center">
            <p class="text-sm font-medium leading-6 dark:text-[#ededed] text-[#0a0a0a]">
              {roleItem.role}
            </p>
            <p class="text-xs leading-5 dark:text-[#737373] text-[#737373]">
              {roleItem.duration.start} - {roleItem.duration.end ?? 'present'}
            </p>
          </div>
          {#if roleItem.skills.length > 0}
          <p class="mt-1 text-xs leading-5 dark:text-[#737373] text-[#737373]">
            {roleItem.skills.join(', ')}
          </p>
          {/if}
        </div>
      {/each}
    </div>
  </li>