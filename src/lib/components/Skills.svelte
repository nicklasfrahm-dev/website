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
		'Svelte'
	];
	const hashtags = $derived.by(() =>
		skills.map((skill) => `#${skill.toLocaleLowerCase()}`).join(' ')
	);
</script>

<!-- TODO: Continue here  -->
<Heading color="text-orange-700 dark:text-orange-500" class="mb-4 text-2xl font-semibold "
	>Skills</Heading
>
<P class="text-lg dark:text-white">
	{hashtags}
</P>
