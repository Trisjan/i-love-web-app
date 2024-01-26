<script>
    import { onMount } from "svelte";
    import { gsap } from "gsap";

	onMount(() => {
		const tl = gsap.timeline();
		const duration = 2;
		
		tl.from('#hero-text', {
			duration,
			opacity: 0
		})
		.from('.box', {
			duration,
			xPercent: 100,
			rotation: -90,
			yPercent: 100,
			ease: 'bounce.out',
		}, `-=${duration * 0.75}`)
	});
</script>

<section>
    <h1 id="hero-text">Trisjan Mustamu</h1>
</section>
<section class="black">

</section>

<style>
    section {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    section:first-child h1 {
        position: relative;
        left: 60%;
    }

    section {
        height: 100vh;
    }
    
    .black {
        background-color: black;
    }

    /* // Medium devices (tablets, 768px and up) */
    @media (min-width: 768px) { 
        
    }

    /* // Large devices (desktops, 992px and up) */
    @media (min-width: 992px) {

    }

    /* // X-Large devices (large desktops, 1200px and up) */
    @media (min-width: 1200px) { 
        
    }
</style>