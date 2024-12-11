<script lang="ts">
	import { Button, Heading, P } from 'flowbite-svelte';

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

<Heading
	tag="h3"
	color="text-orange-700 dark:text-orange-500"
	customSize="text-2xl font-semibold"
	class="mb-2">Recommended reads</Heading
>
<P class="mb-4 text-lg dark:text-white">
	I can't take credit for these, but they've helped me become a better engineer.
</P>
<ul class="flex flex-shrink flex-col">
	{#each recommendations as { title, href, description }}
		<li class="mb-2 inline-block max-w-lg">
			<Button
				tag="a"
				{href}
				target="_blank"
				rel="noopener noreferrer"
				class="block rounded-xl p-4 text-left text-lg font-normal text-black hover:bg-orange-300 dark:text-white  dark:hover:bg-gray-900"
			>
				<Heading tag="h4" color="text-orange-700 dark:text-orange-500" customSize="font-semibold"
					>{title}</Heading
				>
				<P>
					{description}
				</P>
			</Button>
		</li>
	{/each}
</ul>
