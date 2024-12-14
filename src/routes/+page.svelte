<script lang="ts">
	import { Heading, Img, P } from 'flowbite-svelte';
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
				<Heading tag="h1" customSize="text-4xl font-extrabold">
					{name}
				</Heading>
				<Heading
					tag="h2"
					customSize="text-2xl font-bold"
					color="text-orange-700 dark:text-orange-500"
				>
					{title}
				</Heading>
			</div>
			<div>
				<P size="xl">
					{description}
				</P>
			</div>
		</div>
		<div class="flex min-h-64 min-w-64 items-center justify-center">
			<Img
				src="https://github.com/nicklasfrahm.png"
				alt="Nicklas Frahm in Baux with the blurred provence in the background"
				class="h-64 w-64 rounded-full object-cover"
				loading="lazy"
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
