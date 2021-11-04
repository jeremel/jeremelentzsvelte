<svelte:head>
    <title>Jereme Lentz</title>
</svelte:head>

<script>
    import { fade, fly } from 'svelte/transition';
    import { onMount } from 'svelte';

    let ready = false;
    onMount(() => ready = true);
</script>

<!-- {#if ready}
<div class="hero">  
    <h1 in:fade="{{ duration: 2000 }}" ><a href="/webdev">Website Developer</a></h1>
    <h1 in:fade="{{ duration: 2000 }}" ><a href="/consulting">Small Business Consultant</a></h1>
    <h1 in:fade="{{ duration: 2000 }}" ><a href="/photography">Photographer</a></h1>    
</div>
{/if} -->
<main>
    <p>Hi, my name is Jereme Lentz, and I am a freelance <a href="/webdev">website designer and developer</a>, <a href="consulting">small business consultant</a>, and <a href="/photography">photographer</a> located in Egg Harbor City in the <span class="pine"><a href="https://en.wikipedia.org/wiki/Pine_Barrens_(New_Jersey)">pine barrens</a></span> of Atlantic County, New Jersey.</p>
    <p>Find out more <a href="/about">About Me</a> Here!</p>
</main>

<style>
    .hero {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
    }

    .hero h1 {
        margin: 2rem 0;
        padding: 0;
        font-size: 4rem;
    }

    .hero h1 a {
        color: rgb(56, 51, 51);
        text-decoration: none;
        transition: color 500ms;
    }
    
    .hero h1 a:hover {
        color: #F87B72;
    }

    main {
        margin: 2rem 12rem;
    }

    main p {
        margin: 0;
        padding: 1rem 0;
        font-size: 2rem;
    }

    main p a:active {
        color: #F87B72;
    }

    .pine a {
        color: forestgreen;
    }

    .pine a:hover {
        color: darkgreen;
        font-weight: 500;
    }
</style>