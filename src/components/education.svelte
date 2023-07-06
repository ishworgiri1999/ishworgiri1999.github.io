<script>
    export let major='';
    export let school=''
    export let imageUrl=''
    export let address=''
    export let duration={start:''}
</script>
<li class="flex justify-between gap-x-6 py-5">
    <div class="flex gap-x-4">
        {#if imageUrl}
        <img
          class="h-12 w-12 flex-none rounded-full dark:bg-gray-900  bg-gray-50"
          src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
          alt=""
        />
        {:else}
        <div
        class="h-12 w-12 flex items-center justify-center rounded-full dark:bg-gray-900 bg-gray-50"
      ><span>{school?school[0].toUpperCase():''}</span></div>
        {/if}
      
      <div class="min-w-0 flex-auto">
        <p class="text-sm font-semibold leading-6  dark:text-gray-100  text-gray-700">
          {school}
        </p>
        <p class="mt-1 truncate text-xs leading-5 dark:text-gray-300  text-gray-500">
          {major}
        </p>
      </div>
    </div>
    <div class="sm:flex sm:flex-col sm:items-end">
      <p class="text-sm leading-6 dark:text-gray-300  text-gray-900">{address}</p>
      <p class="mt-1 text-xs leading-5 dark:text-gray-200  text-gray-500">
        <span>{duration.start} - {duration.end??'present'}</span> 
      </p>
    </div>
  </li>