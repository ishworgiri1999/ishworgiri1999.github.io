<script>
    import "../app.css";
	import { onMount, setContext } from 'svelte';
	import { writable } from 'svelte/store';
	import { browser } from '$app/environment';

	const darkMode = writable(false);

	function updateDarkMode(value) {
		if (!browser) return;
		if (value) {
			document.documentElement.classList.add('dark');
		} else {
			document.documentElement.classList.remove('dark');
		}
		localStorage.setItem('darkMode', value.toString());
	}

	function toggleDarkMode() {
		darkMode.update(value => {
			const newValue = !value;
			updateDarkMode(newValue);
			return newValue;
		});
	}

	onMount(() => {
		// Check localStorage and system preference
		const stored = localStorage.getItem('darkMode');
		let initialValue = false;
		if (stored !== null) {
			initialValue = stored === 'true';
		} else {
			initialValue = window.matchMedia('(prefers-color-scheme: dark)').matches;
		}
		darkMode.set(initialValue);
		updateDarkMode(initialValue);

		// Subscribe to changes only in browser
		const unsubscribe = darkMode.subscribe(value => {
			updateDarkMode(value);
		});

		return unsubscribe;
	});

	setContext('darkMode', {
		darkMode,
		toggleDarkMode
	});
  </script>
  

  <div class="min-h-screen dark:bg-[#0a0a0a] dark:text-[#ededed] bg-white text-[#0a0a0a] relative transition-colors duration-300">
    <slot />
  </div>