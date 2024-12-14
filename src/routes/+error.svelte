<script>
	import { Heading, Img, Button } from 'flowbite-svelte';
	import { page } from '$app/stores';

	const exclamations = [
		'Oh no',
		'Oops',
		'Yikes',
		'Uh oh',
		'Oh dear',
		'Whoops',
		'Oh my',
		'My oh my'
	];
	let exclamation = $state('');

	$effect.pre(() => {
		exclamation = exclamations[Math.floor(Math.random() * exclamations.length)];
	});
</script>

<div class="container mx-auto flex flex-col gap-y-8 p-4 md:p-8">
	<div class="flex justify-center">
		<Heading
			tag="h1"
			color="text-orange-700 dark:text-orange-500"
			customSize="text-4xl font-extrabold"
			class="w-auto whitespace-nowrap text-center"
		>
			{$page.status}
			{$page.error?.message}
		</Heading>
	</div>
	<div class="mx-auto flex aspect-square h-72 w-72 justify-center">
		<Img
			src="/404.png"
			alt="A surprised mushroom with legs and arms"
			class="object-contain"
			loading="lazy"
		/>
	</div>
	{#if exclamation}
		<div class="flex justify-center">
			<Button
				tag="a"
				href="/"
				class="rounded-xl p-4 text-center text-lg font-normal text-black hover:bg-orange-300  dark:text-white dark:hover:bg-gray-900"
			>
				{exclamation}, take me home!
			</Button>
		</div>
	{/if}
</div>
