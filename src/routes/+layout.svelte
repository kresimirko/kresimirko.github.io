<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import { onMount } from 'svelte';

	let { children } = $props();

	onMount(() => {
		function setTheme(themeName: string) {
			localStorage.setItem('theme', themeName);
			document.documentElement.className = themeName;
		}
		// sanitization, I guess
		switch (localStorage.getItem('theme')) {
			case 'theme-light':
				setTheme('theme-light');
				break;
			// I prefer dark tyvm
			case 'theme-dark':
			default:
				setTheme('theme-dark');
				break;
		}
	});
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
