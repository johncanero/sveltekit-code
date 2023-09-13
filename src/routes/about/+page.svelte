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

    <!-- <div class="text-column">
	    <h1>About this app</h1>
        
        <p>
            This is a <a href="https://kit.svelte.dev">SvelteKit</a> app. You can make your own by typing the
            following into your command line and following the prompts:
        </p>

	    <pre>npm create svelte@latest</pre>

        <p>
            The page you're looking at is purely static HTML, with no client-side interactivity needed.
            Because of that, we don't need to load any JavaScript. Try viewing the page's source, or opening
            the devtools network panel and reloading.
        </p>

        <p>
            The <a href="/sverdle">Sverdle</a> page illustrates SvelteKit's data loading and form handling. Try
            using it with JavaScript disabled!
        </p>
    </div> -->

</section>