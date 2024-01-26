<script>
    import { DarkLogo, BigDarkLogo } from '$lib/index'
    import { onMount } from 'svelte'

    onMount(() => {
        const menuButton = document.querySelector('.menu-button')
        const menu = document.querySelector('ul')
        const menuLinks = document.querySelectorAll('li')


    })
</script>

<nav>
    <a href="/"><img src={DarkLogo} class="mobile" alt="logo"></a>
    <a href="/"><img src={BigDarkLogo} class="desktop" alt="logo"></a>
    <ul>
        <li><a href="/blog">we love web</a></li>
        <li><a href="about">about</a></li>
        <li><a href="/contact">contact</a></li>
    </ul>
    <div class="menu-button">
        <svg viewBox="0 0 100 80" width="40" height="40" fill=var(--primary-dark-color)>
            <rect width="100" height="20" rx="10"></rect>
            <rect y="30" width="100" height="20" rx="10"></rect>
            <rect y="60" width="100" height="20" rx="10"></rect>
        </svg>
    </div>
</nav>

<style>
    nav {
        display: flex;
        align-items: center;
        padding: 1em;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 100;
        max-height: 10%;
    }

    .desktop {
        display: none;
    }

    img {
        width: 2.125rem ;
        mix-blend-mode: difference;
    }

    ul {
        display: none;
        mix-blend-mode: difference;
    }

    @media (min-width: 50.5em) {

        nav {
            padding: 3rem 5rem;
        }

        .menu-button {
            display: none;
        }

        .desktop {
            display: flex;
            text-align: left;
            margin-right: auto; /* Voeg deze regel toe om de afbeelding naar links uit te lijnen */
        }

        .mobile {
            display: none;
        }

        img {
            width: 12rem;
        }

        ul {
            display: flex;
            color: var(--primary-dark-color);
            text-decoration: none;
            list-style: none;
            margin-left: auto;
        }

        li {
            margin-left: 3rem;
            font-size: 1.25rem;
        }

        a {
            text-decoration: none;
            font-weight: bold;
            color: var(--primary-dark-color);
            transition: all 0.3s ease-in-out;
        }

        li a:hover {
            color: var(--secondary-dark-color);
        }
    }
</style>