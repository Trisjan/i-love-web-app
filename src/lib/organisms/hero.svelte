<script>
    export let Text;
    export let imgSrc;
    export let imgAlt;
    export let smallText;
    import { onMount } from "svelte";
    import { gsap } from "gsap";


	onMount(() => {
		const duration = 2;
        const delay = 0.5;
		
		gsap.from('#hero-text', {
			duration,
			opacity: 0,
            x: -700,
            delay,
		})

        gsap.from('#small-text', {
            duration,
            opacity: 0,
            x: 700,
            delay,
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
    <div>
        <h1 id="hero-text">{Text}</h1>
        <h4 id="small-text">{smallText}</h4>
    </div>
    <img id="image-logo" src={imgSrc} alt={imgAlt}>
</section>

<style>
    section {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100dvh;
        overflow-x: hidden;
    }

    div {
        flex-direction: column;
    }

    h1 h2 {
        padding: 0 2rem;
    }

    img {
        display: none;
    }

</style>