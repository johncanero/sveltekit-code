<script>
    import svelteKitTrain from '$lib/images/svelteKitTrain.png';
</script>

<svelte:head>
	<title>Home / SvelteKit</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
    <div class='mt-10'>
        <h1 class='text-2xl font-bold text-center'>Welcome to <span class='text-orange-600'>SvelteKit</span></h1>
        <p class='text-center'>Visit <a href="https://kit.svelte.dev" class='text-orange-500 hover:text-orange-600'>kit.svelte.dev</a> to read the documentation</p>
    </div>
    
    <div class='flex justify-center mt-12 md:mt-0'>
        <picture>
            <!-- <source srcset={welcome} type="image/webp" /> -->
            <img width={500} height={500} src={svelteKitTrain} alt="SvelteKit 3D" />
        </picture>
    </div>
</section>

<!-- style -->
<style lang="postcss">
  :global(html) {
    background-color: theme(colors.zinc.900);
  }

  h1, p {
    font-family: 'Poppins', sans-serif;
    color: white;
  }
</style>