<script>
    import sveltekit3D from '$lib/images/svelteKit3D.png';
</script>

<svelte:head>
	<title>SvelteKit Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
    <div class='my-8'>
        <h1 class='font-bold text-2xl text-center'>Welcome to <span class='text-orange-600'>SvelteKit</span></h1>
        <p class='text-center'>Visit <a href="https://kit.svelte.dev" class='text-orange-500 hover:text-orange-600'>kit.svelte.dev</a> to read the documentation</p>
    </div>
    
    <div class='flex justify-center'>
        <picture>
            <!-- <source srcset={welcome} type="image/webp" /> -->
            <img class="max-w-2xl" src={sveltekit3D} alt="Welcome" />
        </picture>
    </div>
</section>

<!-- style -->
<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.50);
  }

  h1, p {
    font-family: 'Poppins', sans-serif;
  }
</style>