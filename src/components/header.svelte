<script>
    let current = '';
</script>

<header>
    <h1>
        <a href="/"
           class="{current === 'index' ? 'active' : ''}" 
           on:click="{() => current = 'index'}"
        >
            Jereme Lentz
        </a>
    </h1>
    <nav>
        <ul>
            <li>
                <a 
                    href="/webdev" 
                    class="{current === 'webdev' ? 'active' : ''}" 
                    on:click="{() => current = 'webdev'}"
                >
                    Websites
                </a>
            </li>
            <li>
                <a 
                    href="/consulting" 
                    class="{current === 'consulting' ? 'active' : ''}" 
                     on:click="{() => current = 'consulting'}"
                >
                    Consulting
                </a>
            </li>
            <li>
                <a 
                    href="/photography" 
                    class="{current === 'photography' ? 'active' : ''}" 
                     on:click="{() => current = 'photography'}"
                >
                    Photography
                </a>
            </li>
            <li>
                <a 
                    href="/contact" 
                    class="{current === 'contact' ? 'active' : ''}" 
                     on:click="{() => current = 'contact'}"
                >
                    Contact
                </a>
            </li>
        </ul>
    </nav>
</header>

<style>
    header {
        background-image: url("/AC-Skyline.jpg"); 
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
        background-color: #FFF;
        height: 50vh;
        padding: 2rem 4rem;
        margin: 0;
        display: flex;
        justify-content: space-between;
        opacity: 0.9;
    }

    header h1 { 
        font-size: 3rem;
        padding: 0;
        margin: 0;
        color: #F87B72;
    }

    header h1 a {
        color: #F87B72;
        text-decoration: none;
    }

    nav ul {
        list-style: none;
        display: flex;
        flex-wrap: wrap;
        gap: 1rem;
    }

    nav ul li {
        font-size: 1.5rem;
    }

    nav ul li a {
        color: #F87B72;
        text-decoration: none;
        transition: color 333ms;
    }

    nav ul li a:hover {
        text-decoration: underline;
    }

    nav ul li a:active {
        color: coral;
    }

    ul li a.active {
       text-decoration: underline;
       font-weight: 600;
    }
</style>