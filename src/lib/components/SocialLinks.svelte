<script lang="ts">
	import { Button } from 'flowbite-svelte';
	import { LinkedinSolid, GithubSolid } from 'flowbite-svelte-icons';

	const links = [
		{
			name: 'GitHub',
			href: 'https://github.com/nicklasfrahm',
			Icon: GithubSolid,
		},
		{
			name: 'LinkedIn',
			href: 'https://www.linkedin.com/in/nicklasfrahm',
			Icon: LinkedinSolid,
		},
	];
</script>

<ul class="flex items-center justify-start gap-4">
	{#each links as { name, href, Icon }}
		<li class="rounded-xl">
			<Button
				tag="a"
				{href}
				target="_blank"
				rel="noopener noreferrer"
				class="p-2 hover:bg-orange-300 hover:dark:bg-gray-900"
			>
				<span class="sr-only">{name}</span>
				<Icon size="xl" class="text-gray-900 dark:text-white" />
			</Button>
		</li>
	{/each}
</ul>
