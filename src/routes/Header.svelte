<script>
    import { page } from "$app/stores";
    import { onMount } from "svelte";
    import svelteIcon from '$lib/images/svelteIcon.png';
    import githubIcon from '$lib/images/githubIcon.png';

    // Highliting Navbar Links
  const navs = [
    {
      title: "Home",
      href: "/",
    },
    {
      title: "About",
      href: "/about",
    },
  ];

  
  $: url = $page.url.href;
  $: routeId = $page.url.pathname;
</script>

  


<nav class='p-6 bg-zinc-50'>
    <div class='flex justify-between'>
        <div class='flex'>
            <picture class='mr-12'>
                <a href="/">
                    <img width={36} height={36} src={svelteIcon} alt="SvelteKit Icon" />
                </a>
            </picture>
            
            <ul class='hidden mt-1 md:flex gap-x-10'>
                {#each navs as { title, href }}
                <li>
                    <a
                    {href}
                    class:active={href === "/" ? routeId === "/" : url.includes(href)}
                    class='font-medium text-md hover:text-orange-500'
                    {title}>
                        {title}
                    </a>
                 </li>
                {/each}
            </ul>
        </div>
      
        <picture class='hidden md:block'>
            <a href="https://github.com/sveltejs/kit" target="_blank">
                <img width={36} height={36} src={githubIcon} alt="SvelteKit Icon" />
            </a>
        </picture>
    </div>
</nav>

<style>
 .active {
    color: #ea580c;
  }
</style>