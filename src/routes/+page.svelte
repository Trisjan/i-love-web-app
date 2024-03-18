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
            duration: 2,
            delay: 0.8,
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
            delay: 0.8,
        })

        gsap.to("#workimg", {
            scrollTrigger: {
                trigger: "#section2",
                start: "top center",
                end: "bottom center",
                // scrub: true,
                markers: true,
            },
            xPercent: -150,
            duration: 1,
            rotation: 0,
        })
    })
</script>

<Hero
    Text="trisjan mustamu"
    smallText="frontend developer / designer"
    />
<section id="section2">
    <div>
        <h2>experience</h2>
    </div>
    <div class="jobs">
        <div>
            <h3>Albert Heijn</h3>
            <p class="title">Parttime</p>
            <p class="description">Een logistiek medewerker die de goederenstromen binnen een supermarkt coördineert, 
                klanten ondersteunt en adviseert op basis van hun eerdere koopgedrag.</p>
            <p class="date">feb. 2022 - heden</p>
        </div>
        <div>
            <h3>Alphabet</h3>
            <p class="title">Parttime</p>
            <p class="description">Auto ophaal- en leveringsprofessional heb ik auto's getransporteerd naar zowel particulieren als bedrijven. Bij deze
                service hoort ook het reinigen van de auto en deze vlekkeloos te leveren aan de klant.</p>
            <p class="date">feb. 2017 - heden</p>
        </div>
        <div>
            <h3>Use IT B.V.</h3>
            <p class="title">Stage</p>
            <p class="description">Servicedesk medewerker</p>
            <p class="date">feb. 2020 - jun. 2020</p>
        </div>
        <div>
            <h3>NDI ICT Solutions</h3>
            <p class="title">Stage</p>
            <p class="description">Ik heb met name mee gedaan aan het uitvoeren van projecten bij de klanten van dit bedrijf. 
                Hier bij heb ik allerlei netwerken aangelegd en contact gehad met de klanten. 
                Ik ben met name naar locaties geweest als Rotterdam (Delftse Poort), Den Haag (Babylon) etc.</p>
            <p class="date">aug. 2018 - feb. 2019</p>
        </div>
    </div>
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
        min-height: 100vh;
        width: 100%;
    }
    
    section:nth-of-type(even) {
        background-color: var(--secondary-light-color);
    }

    #section2 {
        flex-direction: column;
        gap: 0;
        padding: 5rem 5rem;
    }

    #section2 .jobs div {
        min-height: 33vh;
    }

    #section2 .jobs div .title {
        font-weight: 500;
        font-size: 1.5rem;
    }

    #section2 .jobs div .description {
        max-width: 70%;
    }

    #section2 .jobs div .date {
        font-weight: 400;
        font-size: 0.9rem;
    }

    /* // Large devices (desktops, 992px and up) */
    @media (min-width: 992px) {
        section {
            flex-direction: row;
            justify-content: space-around;
            align-items: center;
        }

        #section2 {
            position: relative;
        }
    }
</style>