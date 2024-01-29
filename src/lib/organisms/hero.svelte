<script>
    export let Text;
    export let imgSrc;
    export let imgAlt;
    import { onMount } from "svelte";
    import { gsap } from "gsap";

	onMount(() => {
		const tl = gsap.timeline();
		const duration = 2;
		
		tl.from('#hero-text', {
			duration,
			opacity: 0,
            x: -700,
            delay: 1,
		})

        gsap.from("#image-logo", {
        duration: 0.5,
        delay: 1,
        scale: 0,
        // stagger: 1,
        })
	});
</script>

<section>
    <h1 id="hero-text">{Text}</h1>
    <img id="image-logo" src={imgSrc} alt={imgAlt}>
</section>

<style>
    section {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100dvh;
    }

    h1 {
        padding: 0 2rem;
    }

    img {
        display: none;
    }

    @media (min-width: 768px) {
        section {

        }
    }
</style>