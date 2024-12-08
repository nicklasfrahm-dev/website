<script lang="ts">
	import { Button } from 'flowbite-svelte';

	const recommendations = [
		{
			title: 'Twelve-Factor App',
			href: 'https://12factor.net/',
			description: 'A methodology for building modern, scalable, maintainable software.'
		},
		{
			title: 'Conventional Commits',
			href: 'https://www.conventionalcommits.org/',
			description:
				'A specification for adding human and machine readable meaning to commit messages.'
		}
	];
</script>

<h3 class="py-2 text-2xl font-semibold dark:text-white">Recommended reads</h3>
<h4 class="mb-4 text-lg dark:text-white">
	I can't take credit for these, but they've helped me become a better engineer.
</h4>
<ul class="flex flex-shrink flex-col">
	{#each recommendations as { title, href, description }}
		<li class="mb-2 inline-block max-w-lg">
			<Button
				tag="a"
				{href}
				target="_blank"
				rel="noopener noreferrer"
				class="block rounded-xl p-4 text-left text-orange-700 hover:bg-orange-300 dark:text-orange-500 dark:hover:bg-gray-900"
			>
				<span class="font-semibold">{title}</span>
				<p class="text-lg text-black dark:text-white">
					{description}
				</p>
			</Button>
		</li>
	{/each}
</ul>
