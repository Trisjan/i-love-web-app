<script>
    let notActive = false;

    import { DarkLogo, BigDarkLogo } from '$lib/index'
    import { onMount } from 'svelte'
    import { gsap } from 'gsap'

    onMount(() => {
        const menuButton = document.querySelector('.menu-button')
        const menu = document.querySelector('.nav-items')
        menuButton.addEventListener('click', () => {
            menu.classList.toggle('active')
        })

    let tl = gsap.timeline();

    tl.from('nav', {
        duration: 2,
        opacity: 0,
        y: -300,
    })

    })
</script>

<nav>
    <a href="/"><img src={DarkLogo} class="mobile" alt="logo"></a>
    <a href="/"><img src={BigDarkLogo} class="desktop" alt="logo"></a>
    <!-- class:active={notActive} houdt in dat de class active in de css wordt toegewezen, echter wil ik niet dat deze aanstaat. Als ik de class niet mee geef
    denkt sveltekit dat hij niet gebruikt wordt waardoor hij door treeshaking niet wordt meegenomen bij de live result. Door er een variabele mee te geven
    die standaard op false staat krijgt hij de class mee maar is hij false dus staat hij standaard niet aan.-->     
    <ul class="nav-items" class:active={notActive}>
        <li><a href="/blog">we love web</a></li>
        <li><a href="about">about</a></li>
        <li><a href="/contact">contact</a></li>
    </ul>
    <div class="menu-button" class:open={notActive}>
        <svg width="3.5rem" height="3.5rem" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M4 18L20 18" stroke="#000000" stroke-width="2" stroke-linecap="round"/>
            <path d="M4 12L20 12" stroke="#000000" stroke-width="2" stroke-linecap="round"/>
            <path d="M4 6L20 6" stroke="#000000" stroke-width="2" stroke-linecap="round"/>
        </svg>
    </div>
</nav>

<style>
    nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 1rem 2rem;
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
        width: 3rem ;
        mix-blend-mode: difference;
    }

    .nav-items {
        display: none;
        text-align: left;
        mix-blend-mode: difference;
        list-style: none;
    }
    

    .active {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: var(--secondary-dark-color);
        z-index: 1;
        margin-top: 5rem;
    }

    .menu-button {
        display: block;
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

        .nav-items {
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