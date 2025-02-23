<script lang="ts">
	import { Navbar, NavBrand, DarkMode } from 'flowbite-svelte';
	import '../app.css';

	let { children } = $props();
</script>

<Navbar class="shadow dark:bg-gray-900">
	<NavBrand href="/">
		<span
			class="self-center text-xl font-semibold whitespace-nowrap text-orange-700 dark:text-orange-500"
			>nicklasfrahm.dev</span
		>
	</NavBrand>
	<DarkMode class="self-center" />
</Navbar>

{@render children()}
