<script>
    import { page } from "$app/stores";
    import { onMount } from "svelte";
    import svelteIcon from '$lib/images/svelteIcon.png';
    import 'iconify-icon'

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

<nav class='px-6 py-4 bg-orange-600 bg-opacity-95'>
    <div class='flex justify-between'>
        <div class='flex'>
            <picture class='mr-16'>
                <a href="/">
                    <img width={36} height={36} src={svelteIcon} alt="SvelteKit Icon" />
                </a>
            </picture>
            
            <ul class='hidden mt-1 md:flex md:gap-x-12'>
                {#each navs as { title, href }}
                <li>
                    <a
                    {href}
                    class:active={href === "/" ? routeId === "/" : url.includes(href)}
                    class='font-medium text-md text-neutral-900 hover:text-neutral-50'
                    {title}>
                        {title}
                    </a>
                 </li>
                {/each}
            </ul>
        </div>
      
        <picture class='hidden md:block'>
            <a href="https://github.com/sveltejs/kit" target="_blank">
                <iconify-icon icon="mdi:github" style="font-size: 36px" class='text-white hover:text-black'></iconify-icon>
            </a>
        </picture>

            <ul class='flex mt-1 md:hidden gap-x-6'>
                {#each navs as { title, href }}
                <li>
                    <a
                    {href}
                    class:active={href === "/" ? routeId === "/" : url.includes(href)}
                    class='font-medium text-md text-neutral-900 hover:text-neutral-50'
                    {title}>
                        {title}
                    </a>
                 </li>
                {/each}
            </ul>
    </div>
    
</nav>

<style>
 .active {
    color: #fff;
  }
</style>