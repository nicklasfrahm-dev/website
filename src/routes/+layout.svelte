<script lang="ts">
	import { Navbar, NavBrand, DarkMode } from 'flowbite-svelte';
	import '../app.css';

	let { children } = $props();
</script>

<Navbar class="shadow dark:bg-gray-900">
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
			>nicklasfrahm.dev</span
		>
	</NavBrand>
	<DarkMode class="self-center" />
</Navbar>

{@render children()}
