<script>
    import Header from "../components/header.svelte";
    import Footer from "../components/footer.svelte";
</script>

<style>
    main {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>

<Header />
<main>
    <slot />
</main>
<Footer />
