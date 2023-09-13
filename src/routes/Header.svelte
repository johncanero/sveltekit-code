<script>
    import svelteIcon from '$lib/images/svelteIcon.png';
    import githubIcon from '$lib/images/githubIcon.png';
</script>

<navbar class='m-6'>
    <div class='flex justify-between'>
        <div class='flex'>
            <picture class='mr-12'>
                <a href="/">
                    <img width={36} height={36} src={svelteIcon} alt="SvelteKit Icon" />
                </a>
            </picture>
            
            <!-- Indicate Highlight of the LINK tag -->
            <ul class='hidden mt-1 md:flex gap-x-10'>
                <li>
                    <a href="/" class='font-medium hover:text-orange-600'>Home</a>
                </li>
                <li>
                    <a href="/about" class='font-medium hover:text-orange-600'>About</a>
                </li>
            </ul>
        </div>
      
        <picture class='hidden md:block'>
            <a href="https://github.com/sveltejs/kit" target="_blank">
                <img width={36} height={36} src={githubIcon} alt="SvelteKit Icon" />
            </a>
        </picture>
    </div>
</navbar>

<style>
    
</style>