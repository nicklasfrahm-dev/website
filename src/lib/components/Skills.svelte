<script lang="ts">
	import { Heading, P } from 'flowbite-svelte';
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
		'Svelte',
	];
	const hashtags = $derived.by(() =>
		skills.map((skill) => `#${skill.toLocaleLowerCase()}`).join(' '),
	);
</script>

<Heading
	color="text-orange-700 dark:text-orange-500"
	customSize="text-2xl font-semibold"
	class="mb-4"
>
	Skills
</Heading>
<P size="xl">
	{hashtags}
</P>
