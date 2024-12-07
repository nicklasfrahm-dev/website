<script lang="ts">
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, DarkMode } from 'flowbite-svelte';
	import '../app.css';

	let { children } = $props();
</script>

<Navbar class="shadow dark:bg-gray-900">
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">nicklasfrahm.dev</span>
	</NavBrand>
	<NavHamburger />
	<div class="flex align-center justify-between flex-grow ml-4">
		<NavUl>
			<NavLi href="/">Home</NavLi>
		</NavUl>
		<DarkMode class="self-center"/>
	</div>
</Navbar>

{@render children()}
