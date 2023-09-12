<script>
    import svelteIcon from '$lib/images/svelteIcon.png';
    import githubIcon from '$lib/images/githubIcon.png';
</script>

<navbar class='m-4'>
    <div class='flex justify-between'>
        <picture>
            <a href="https://kit.svelte.dev/" target="_blank">
                <img width={36} height={36} src={svelteIcon} alt="SvelteKit Icon" />
            </a>
        </picture>

        <picture class='hidden md:block'>
            <a href="https://github.com/sveltejs/kit" target="_blank">
                <img width={36} height={36} src={githubIcon} alt="SvelteKit Icon" />
            </a>
        </picture>
    </div>
</navbar>
