<svelte:head>
    <title>Jereme Lentz Photography</title>
</svelte:head>

<script>
	import { fade } from 'svelte/transition';
    import { onMount } from 'svelte';

    let ready = false;
    onMount(() => ready = true);

    function handleClick(e) {
        const src = e.currentTarget.src;
        console.log(src);
    }
</script>

<main>
    <h1>Photography</h1>
    <p>I work with businesses in South Jersey to create websites that are unique and that drive sales and conversions through my web development company, <span class="design">Lentz Design Co.</span></p>
    
    {#if ready}
    <div class="images" in:fade="{{ duration: 2000 }}">  
        <img on:click={handleClick} src="images/vinyl-brewery.jpg" alt="Vinyl Brewery, Hammonton, NJ" />
        <img on:click={handleClick} src="images/ireland-cliffs-of-moher.jpg" alt="Cliffs of Moher in Ireland" />
        <img on:click={handleClick} src="images/paul-tammany.jpg" alt="Mount Tammany, New Jersey" />
        <img on:click={handleClick} src="images/dubrovnik-croatia.jpg" alt="Dubrovnik, Croatia" /> 
    </div>
    {/if}

    <p><a href="/contact">Contact Me</a> today if you are interested in my photography.</p>
</main>

<style>
    main {
        margin: 2rem 12rem;
    }

    main p {
        margin: 0;
        padding: 1rem 0;
        font-size: 2rem;
    }

    .images {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 1rem;
    }

    .images img {
        width: 100%;
        height: 100%;
        border-radius: 1%;
    }

</style>