<script>
    import sveltekit3D from '$lib/images/svelteKit3D.png';
</script>

<svelte:head>
	<title>About / SvelteKit</title>
	<meta name="description" content="About this app" />
</svelte:head>

<section>
    <div>
        <h1 class='text-2xl font-bold text-center'>About</h1>
        <p class='text-center'>Visit <a href="https://kit.svelte.dev" class='text-orange-500 hover:text-orange-600'>kit.svelte.dev</a> to read the documentation</p>
    </div>

      <div class='flex justify-center'>
        <picture>
            <!-- <source srcset={welcome} type="image/webp" /> -->
            <img width={600} height={600} src={sveltekit3D} alt="SvelteKit 3D" />
        </picture>
    </div>
</section>