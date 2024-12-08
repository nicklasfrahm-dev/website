<script lang="ts">
	import RecommendReads from '$lib/components/RecommendReads.svelte';
	import SocialLinks from '$lib/components/SocialLinks.svelte';
	import Skills from '$lib/components/Skills.svelte';

	const name = 'Nicklas Frahm';
	const title = 'Platform Engineer';
	const description = `I'm a platform engineer with a passion for networking and sustainability. I've been
  working with Kubernetes and cloud-native technologies for more than 5 years.`;
</script>

<div class="container mx-auto flex flex-col gap-y-8 p-4 md:p-8">
	<section class="flex flex-col gap-8 md:flex-row">
		<div class="flex flex-col gap-4">
			<div>
				<h1 class="self-center whitespace-nowrap text-4xl font-bold dark:text-white">
					{name}
				</h1>
				<h2 class="self-center whitespace-nowrap text-2xl font-light dark:text-white">
					{title}
				</h2>
			</div>
			<div>
				<p class="text-lg dark:text-white">
					{description}
				</p>
			</div>
		</div>
		<div class="flex min-h-64 min-w-64 justify-center">
			<img
				src="https://github.com/nicklasfrahm.png"
				alt="Nicklas Frahm"
				class="h-64 w-64 rounded-full object-cover"
			/>
		</div>
		<div class="flex flex-col gap-4">
			<div>
				<Skills />
			</div>
			<div>
				<SocialLinks />
			</div>
		</div>
	</section>
	<section>
		<RecommendReads />
	</section>
</div>
