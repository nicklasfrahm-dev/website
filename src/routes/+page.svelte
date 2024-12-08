<script lang="ts">
	import { GithubSolid, LinkedinSolid } from 'flowbite-svelte-icons';
	const links = [
		{
			name: 'GitHub',
			href: 'https://github.com/nicklasfrahm',
			Icon: GithubSolid
		},
		{
			name: 'LinkedIn',
			href: 'https://www.linkedin.com/in/nicklasfrahm',
			Icon: LinkedinSolid
		}
	];
	const skills = [
		'Kubernetes',
		'Golang',
		'Networking',
		'Linux',
		'Bash',
		'Helm',
		'Prometheus',
		'Grafana',
		'Loki',
		'GitOps',
		'Node',
		'React',
		'Svelte'
	];
	const hashtags = $derived.by(() =>
		skills.map((skill) => `#${skill.toLocaleLowerCase()}`).join(' ')
	);
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

<div class="container mx-auto p-8">
	<section class="flex flex-col md:flex-row">
		<div class="flex flex-col">
			<div class="py-4">
				<h1 class="self-center whitespace-nowrap text-4xl font-bold dark:text-white">
					Nicklas Frahm
				</h1>
				<h2 class="self-center whitespace-nowrap text-xl font-light dark:text-white">
					Platform Engineer
				</h2>
			</div>
			<div class="py-4">
				<p class="text-lg dark:text-white">
					I'm a platform engineer with a passion for networking and sustainability. I've been
					working with Kubernetes and cloud-native technologies for more than 5 years.
				</p>
			</div>
		</div>
		<div class="mx-4 flex min-h-64 min-w-64 justify-center">
			<img
				src="https://github.com/nicklasfrahm.png"
				alt="Nicklas Frahm"
				class="h-64 w-64 rounded-full object-cover"
			/>
		</div>
		<div class="flex flex-col">
			<div class="py-4">
				<h3 class="mb-2 text-2xl font-semibold dark:text-white">Skills</h3>
				<p class="text-lg dark:text-white">
					{hashtags}
				</p>
			</div>
			<div class="py-4">
				<ul class="flex justify-start">
					{#each links as { name, href, Icon }}
						<li class="mr-4">
							<a {href} target="_blank" rel="noopener noreferrer">
								<span class="sr-only">{name}</span>
								<Icon size="xl" class="text-gray-900 dark:text-white" />
							</a>
						</li>
					{/each}
				</ul>
			</div>
		</div>
	</section>
	<section>
		<h3 class="py-2 text-2xl font-semibold dark:text-white">Recommended reads</h3>
		<h4 class="mb-4 text-lg dark:text-white">
			I can't take credit for these, but they've helped me become a better engineer.
		</h4>
		<ul>
			{#each recommendations as { title, href, description }}
				<li class="py-2">
					<a
						{href}
						target="_blank"
						rel="noopener noreferrer"
						class="text-blue-500 dark:text-blue-400"
					>
						{title}
						<p class="text-lg text-black dark:text-white">
							{description}
						</p>
					</a>
				</li>
			{/each}
		</ul>
	</section>
</div>
