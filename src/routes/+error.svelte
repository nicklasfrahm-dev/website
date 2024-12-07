<script>
	import { page } from '$app/stores';

    const exclamations = ['Oh no', 'Oops', 'Yikes', 'Uh oh', 'Oh dear', 'Whoops', 'Oh my', 'My oh my'];
    let exclamation = $state('');

    $effect.pre(() => {
        exclamation = exclamations[Math.floor(Math.random() * exclamations.length)];
    });
</script>

<div class="container mx-auto p-4 flex justify-center flex-col">
    <h1 class="self-center whitespace-nowrap text-4xl font-semibold dark:text-white">
        {$page.status} {$page.error?.message}
    </h1>
    <div class="w-1/4 h-1/4 aspect-square flex justify-center mx-auto">
        <img src="/404.png" alt="A surprised mushroom with legs and arms" class="object-contain" />
    </div>
    {#if exclamation}
        <h2 class="self-center whitespace-nowrap text-2xl dark:text-white">{exclamation}, this is a problem!</h2>
    {/if}
</div>