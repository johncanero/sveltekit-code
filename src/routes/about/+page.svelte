<script>
    import sveltekit3D from '$lib/images/svelteKit3D.png';
</script>

<svelte:head>
	<title>About / SvelteKit</title>
	<meta name="description" content="About this app" />
</svelte:head>

<section>
    <div>
        <h1 class='mt-10 text-2xl font-bold text-center'>About</h1>
        <p class='text-center'>Visit <a href="https://kit.svelte.dev" class='text-orange-500 hover:text-orange-600'>kit.svelte.dev</a> to read the documentation</p>
    </div>

    <div class='flex justify-center'>
        <picture>
            <!-- <source srcset={welcome} type="image/webp" /> -->
            <img width={600} height={600} src={sveltekit3D} alt="SvelteKit 3D" />
        </picture>
    </div>

    <div class='mb-12'>
        <p>
            This is a <a href="https://kit.svelte.dev" class='text-orange-600 hover:underline'>SvelteKit</a> app. You can make your own by typing the
            following into your command line and following the prompts:
        </p>

        <div class='p-8 mt-4 rounded-2xl bg-neutral-900'>
            <pre class='text-white'>npm create svelte@latest my-app</pre>
            <pre class='text-white'>cd my-app</pre>
            <pre class='text-white'>npm install</pre>
            <pre class='text-white'>npm run dev</pre>
            
        </div>

        <p class='mt-4'>
            The page you're looking at is purely static HTML, with no client-side interactivity needed.
            Because of that, we don't need to load any JavaScript. Try viewing the page's source, or opening
            the devtools network panel and reloading.
        </p>
    </div>
</section>


<!-- style -->
<style>
  h1, p {
    font-family: 'Poppins', sans-serif;
  }
</style>