<script>
    import "./app.css"
    import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
    import '@fontsource/poppins';
</script>

<div class='flex flex-col min-h-screen'>
    <Header />
    
    <main class='box-border flex flex-col flex-1 w-full max-w-screen-lg p-4 mx-auto'>
        <slot />
    </main>

	<Footer />
</div>
