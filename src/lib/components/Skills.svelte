<script lang="ts">
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

<h3 class="mb-2 text-2xl font-semibold dark:text-white">Skills</h3>
<p class="text-lg dark:text-white">
	{hashtags}
</p>
