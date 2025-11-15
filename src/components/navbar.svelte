<script>
      let showDialog = false;

      export let toggleDarkMode;
      export let darkMode;

const navs = [
  { title: "Work", href: "#work" },
  { title: "Education", href: "#education" },
  { title: "Projects", href: "#project" },

];
</script>

<header class="absolute inset-x-0 top-0 z-50 backdrop-blur-sm bg-white/80 dark:bg-[#0a0a0a]/80 border-b border-[#e5e5e5] dark:border-[#262626]">
    <nav
      class="flex items-center justify-between p-6 lg:px-8"
      aria-label="Global"
    >
      <div class="flex ">
        <a href="/" class="-m-1.5 p-1.5">
          <span class="sr-only">Your Company</span>
          <img
            class="h-12 w-auto"
            src="/logo.png"
            alt=""
          />
        </a>
      </div>
     
      <div class="hidden lg:flex lg:gap-x-12 items-center">
        {#each navs as nav}
          <a
            href={nav.href}
            class="text-sm font-medium leading-6 dark:text-[#ededed] text-[#0a0a0a] hover:opacity-60 transition-opacity">{nav.title}</a
          >
        {/each}
        <button
          on:click={toggleDarkMode}
          type="button"
          class="ml-4 p-2 rounded-lg border border-[#e5e5e5] dark:border-[#262626] bg-white dark:bg-[#0a0a0a] hover:bg-[#fafafa] dark:hover:bg-[#171717] transition-colors"
          aria-label="Toggle dark mode"
        >
          {#if darkMode}
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
            </svg>
          {:else}
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" />
            </svg>
          {/if}
        </button>
      </div>
      <div class="flex lg:hidden items-center gap-2">
        <button
          on:click={toggleDarkMode}
          type="button"
          class="p-2 rounded-lg border border-[#e5e5e5] dark:border-[#262626] bg-white dark:bg-[#0a0a0a] hover:bg-[#fafafa] dark:hover:bg-[#171717] transition-colors"
          aria-label="Toggle dark mode"
        >
          {#if darkMode}
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
            </svg>
          {:else}
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" />
            </svg>
          {/if}
        </button>
        <button
          on:click={() => (showDialog = true)}
          type="button"
          class="-m-2.5 inline-flex items-center justify-center rounded-lg p-2.5 dark:text-[#ededed] text-[#0a0a0a] hover:bg-[#fafafa] dark:hover:bg-[#171717] transition-colors"
        >
          <span class="sr-only">Open main menu</span>
          <svg
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            aria-hidden="true"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
            />
          </svg>
        </button>
      </div>
    </nav>
    <!-- Mobile menu, show/hide based on menu open state. -->
    <div
      class="{showDialog ? '' : 'hidden'} lg:hidden"
      role="dialog"
      aria-modal="true"
    >
      <!-- Background backdrop, show/hide based on slide-over state. -->
      <div class="fixed inset-0 z-50" />
      <div
        class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto dark:bg-[#0a0a0a] bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-[#e5e5e5] dark:sm:ring-[#262626]"
      >
        <div class="flex items-center justify-between">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Ishwor Giri</span>
            <img
              class="h-12 w-auto"
              src="/logo.png"
              alt=""
            />
          </a>
          <button
            on:click={() => (showDialog = false)}
            type="button"
            class="-m-2.5 rounded-lg p-2.5 dark:text-[#ededed] text-[#0a0a0a] hover:bg-[#fafafa] dark:hover:bg-[#171717] transition-colors"
          >
            <span class="sr-only">Close menu</span>
            <svg
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
        <div class="mt-6 flow-root">
          <div class="-my-6 divide-y divide-[#e5e5e5] dark:divide-[#262626]">
            <div class="space-y-2 py-6">
              {#each navs as nav}
                <a
                  href={nav.href}
                  on:click={() => (showDialog = false)}
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-medium leading-7 dark:text-[#ededed] text-[#0a0a0a] hover:bg-[#fafafa] dark:hover:bg-[#171717] transition-colors"
                  >{nav.title}</a
                >
              {/each}
              <button
                on:click={toggleDarkMode}
                type="button"
                class="-mx-3 w-full text-left block rounded-lg px-3 py-2 text-base font-medium leading-7 dark:text-[#ededed] text-[#0a0a0a] hover:bg-[#fafafa] dark:hover:bg-[#171717] transition-colors flex items-center gap-2"
              >
                {#if darkMode}
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
                  </svg>
                  Light Mode
                {:else}
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" />
                  </svg>
                  Dark Mode
                {/if}
              </button>
            </div>
            
          </div>
        </div>
      </div>
    </div>
  </header>
