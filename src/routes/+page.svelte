<script>
    import { Hero, PrimaryWorkPhoto } from "$lib";
    import { onMount } from "svelte";
    import { gsap } from "gsap/dist/gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger";

    onMount(() => {
        gsap.registerPlugin(ScrollTrigger);

        gsap.from("h2", {
            scrollTrigger: {
                trigger: "#section2",
                start: "20% center",
                end: "bottom center",
                // scrub: true,
                markers: true,
            },
            opacity: 0,
            x: -500,
            duration: 2,
        })

        gsap.from("button", {
            scrollTrigger: {
                trigger: "#section2",
                start: "20% center",
                end: "bottom center",
                // scrub: true,
                markers: true,
            },
            opacity: 0,
        })

        gsap.from("img", {
            scrollTrigger: {
                trigger: "#section2",
                start: "20% center",
                end: "bottom center",
                // scrub: true,
                markers: true,
            },
            opacity: 0,
            x: 500,
            duration: 2,
        })
    })
</script>

<Hero
    Text="trisjan mustamu"
    smallText="frontend developer / designer"
    />
<section id="section2">
    <div>
        <h2>my work</h2>
        <button>Go to</button>
    </div>
    <img src={PrimaryWorkPhoto} alt="Logo">
</section>
<section>

</section>

<style>
    section {
        display: flex;
        justify-content: center;
        flex-direction: column;
        gap: 5rem;
        padding: 0 2rem;
    }

    section {
        height: 100vh;
        width: 100%;
    }
    
    section:nth-of-type(even) {
        background-color: var(--secondary-dark-color);
    }

    /* section > h2{
    } */

    section > img {
        max-width: 20%;
        object-fit: cover;
        filter: grayscale(100%);
    }

    button {
        background-color: var(--primary-dark-color);
        color: var(--default-light);
        border: none;
        font-size: 1rem;
        width: 8rem;
        height: 3rem;
        border-radius: 1rem;
        cursor: pointer;
        transition: all 0.5s ease-in-out;
    }

    button:hover {
        transform: scale(1.1);
        box-shadow: 0px 0px 35px -7px rgba(0,0,0,0.9);
        font-weight: bold;
    }

    /* // Large devices (desktops, 992px and up) */
    @media (min-width: 992px) {
        section {
            flex-direction: row;
            justify-content: space-around;
            align-items: center;
        }

        section > img {
            width: 30%;
            object-fit: cover;
            filter: grayscale(100%);
        }
    }
</style>