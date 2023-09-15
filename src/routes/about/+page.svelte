<script>
// @ts-nocheck

    import sveltekit3D from '$lib/images/svelteKit3D.png';

    // copyText functionality   
    function copyText(htmlElement) {
        if (!htmlElement) {
        return;
        }

        let elementText = htmlElement.innerText;

        let inputElement = document.createElement('input');
        inputElement.setAttribute('value', elementText);
        document.body.appendChild(inputElement);

        inputElement.select();

        document.execCommand('copy');
        inputElement.parentNode.removeChild(inputElement);
    }
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

        <div class='p-8 mt-4 rounded-2xl bg-zinc-800'>
            <div class='flex justify-between'>
                <pre id="text" class='text-sm text-white md:text-base'>npm create svelte@latest my-app</pre>
                <button on:click="{() => copyText(document.querySelector('#text'))}">
                    <iconify-icon icon="ph:copy" style="font-size: 20px" class='text-white hover:text-zinc-200'></iconify-icon>
                </button>
            </div>

            <div class='flex justify-between'>
                <pre id="text2" class='text-sm text-white md:text-base'>cd my-app</pre>
                <button on:click="{() => copyText(document.querySelector('#text2'))}">
                    <iconify-icon icon="ph:copy" style="font-size: 20px" class='text-white hover:text-zinc-200'></iconify-icon>
                </button>
            </div>
         
             <div class='flex justify-between'>
                <pre id="text3" class='text-sm text-white md:text-base'>npm install</pre>
                <button on:click="{() => copyText(document.querySelector('#text3'))}">
                    <iconify-icon icon="ph:copy" style="font-size: 20px" class='text-white hover:text-zinc-200'></iconify-icon>
                </button>
            </div>

             <div class='flex justify-between'>
                 <pre id="text3" class='text-sm text-white md:text-base'>npm run dev</pre>
                <button on:click="{() => copyText(document.querySelector('#text3'))}">
                    <iconify-icon icon="ph:copy" style="font-size: 20px" class='text-white hover:text-zinc-200'></iconify-icon>
                </button>
            </div>
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
    color: white;
  }
</style>