<script>
    import { Nav } from "$lib/index.js";
    import { onMount } from "svelte";

    onMount(() => {
        const lenis = new Lenis()

        lenis.on('scroll', (e) => {
        console.log(e)
        })

        function raf(time) {
        lenis.raf(time)
        requestAnimationFrame(raf)
        }

        requestAnimationFrame(raf)
    })
    
</script>

<main>
    <header>
        <Nav/>
    </header>
    <slot/>

</main>

<style>
    @import url('https://fonts.googleapis.com/css2?family=MuseoModerno:ital,wght@0,100..900;1,100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "MuseoModerno", sans-serif;		
        --font-size: 1em;
		--font-scale: 1.250;
    }
</style>