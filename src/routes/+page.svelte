<script>
    import { Hero, AlbertHeijnLogo, AlphabetLogo, NDILogo, UseITLogo, Education, CameraLogo, GameLogo, LocationLogo, MailLogo, PhoneLogo, SportsLogo, BulletPolygon } from "$lib";
    import { onMount } from "svelte";
    import { gsap } from "gsap/dist/gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger";

    onMount(() => {
        gsap.registerPlugin(ScrollTrigger);

        gsap.from("#abouttitle", {
            scrollTrigger: {
                trigger: "#section1",
                start: "top center",
                end: "bottom center",
            },
            xPercent: -300,
            duration: 1,
        })

        gsap.from("#abouttext", {
            scrollTrigger: {
                trigger: "#section1",
                start: "top center",
                end: "bottom center",
            },
            xPercent: -300,
            duration: 1,
        })

        gsap.from("#experiencetitle", {
            scrollTrigger: {
                trigger: "#section2",
                start: "top center",
                end: "bottom center",
            },
            xPercent: -300,
            duration: 1,
        })

        gsap.from("#job1", {
            scrollTrigger: {
                trigger: "#job1",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: -200,
            duration: 1.2,
        })

        gsap.from("#job2", {
            scrollTrigger: {
                trigger: "#job2",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 200,
            duration: 1.2,
        })

        gsap.from("#job3", {
            scrollTrigger: {
                trigger: "#job3",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: -200,
            duration: 1.2,
        })

        gsap.from("#job4", {
            scrollTrigger: {
                trigger: "#job4",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 200,
            duration: 1.2,
        })

        gsap.from("#school1", {
            scrollTrigger: {
                trigger: "#school1",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 100,
            duration: 1.2,
            opacity: 0,
        })

        gsap.from("#school2", {
            scrollTrigger: {
                trigger: "#school2",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 100,
            duration: 1.2,
            opacity: 0,
        })

        gsap.from("#school3", {
            scrollTrigger: {
                trigger: "#school3",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 100,
            duration: 1.2,
            opacity: 0,
        })

        gsap.from("#school4", {
            scrollTrigger: {
                trigger: "#school4",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 100,
            duration: 1.2,
            opacity: 0,
        })

        gsap.from("#school5", {
            scrollTrigger: {
                trigger: "#school5",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 100,
            duration: 1.2,
            opacity: 0,
        })

        gsap.from("#contact", {
            scrollTrigger: {
                trigger: "#section4",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: -100,
            duration: 1,
        })

        gsap.from("#skills", {
            scrollTrigger: {
                trigger: "#section4",
                start: "top 70%",
                end: "bottom center",
            },
            yPercent: 200,
            duration: 1,
        })

        gsap.from("#hobbys", {
            scrollTrigger: {
                trigger: "#section4",
                start: "top 70%",
                end: "bottom center",
            },
            xPercent: 100,
            duration: 1,
        })
    })
</script>

<Hero
    Text="trisjan mustamu"
    smallText="frontend developer / designer"
    />
<section id="section1">
    <h2 id="abouttitle">About me</h2>
    <p id="abouttext">"Altijd nieuwsgierig en klaar voor nieuwe uitdagingen in mijn carrière, ben ik opgewonden om mijn vaardigheden van tijdens mijn studie te gebruiken en echt iets te bereiken. 
        Ik ben enthousiast om mijn opgedane vaardigheden tijdens mijn studie in te zetten en een betekenisvolle bijdrage te leveren in mijn vakgebied.
        Mijn doel is om niet alleen professioneel te groeien, maar ook om mijn kennis en expertise in te zetten voor het van anderen.
        Ik ben vastbesloten om mijn potentieel te benutten en een verder te groeien."</p>
</section>
<section id="section2">
    <div>
        <h2 id="experiencetitle">experience</h2>
    </div>
    <div class="jobs">
        <div id="job1">
            <div class="logo">
                <img src={AlbertHeijnLogo} alt="albert heijn">
            </div>
            <div class="info">
                <h3>Albert Heijn</h3>
                <p class="title">Parttime</p>
                <p class="description">Een logistiek medewerker die de goederenstromen binnen een supermarkt coördineert, 
                    klanten ondersteunt en adviseert op basis van hun eerdere koopgedrag.</p>
                <p class="date">feb. 2022 - heden</p>
            </div>
        </div>
        <div id="job2">
            <div class="logo">
                <img src={AlphabetLogo} alt="alphabet" loading="lazy">
            </div>
            <div class="info">
                <h3>Alphabet</h3>
                <p class="title">Parttime</p>
                <p class="description">Auto ophaal- en leveringsprofessional waar ik auto's getransporteerd naar zowel particulieren als bedrijven. Bij deze
                    service hoort ook het reinigen van de auto en deze vlekkeloos te leveren aan de klant.</p>
                <p class="date">feb. 2017 - heden</p>
            </div>
        </div>
        <div id="job3">
            <div class="logo">
                <img src={UseITLogo} alt="use it">
            </div>
            <div class="info">
                <h3>Use IT B.V.</h3>
                <p class="title">Stage</p>
                <p class="description">Servicedesk medewerker</p>
                <p class="date">feb. 2020 - jun. 2020</p>
            </div>
        </div>
        <div id="job4">
            <div class="logo">
                <img src={NDILogo} alt="ndi">
            </div>
            <div class="info">
                <h3>NDI ICT Solutions</h3>
                <p class="title">Stage</p>
                <p class="description">Ik heb met name mee gedaan aan het uitvoeren van projecten bij de klanten van dit bedrijf. 
                    Hier bij heb ik allerlei netwerken aangelegd en contact gehad met de klanten. 
                    Ik ben met name naar locaties geweest als Rotterdam (Delftse Poort), Den Haag (Babylon) etc.</p>
                <p class="date">aug. 2018 - feb. 2019</p>
            </div>
        </div>
    </div>
</section>
<section id="section3">
    <div class="section_title">
        <h2 class="educationtitle">education</h2>
        <img src={Education} alt="education icon big">
    </div>
    <div class="education">
        <div id="school1">
            <div class="info">
                <h3>Hogeschool van Amsterdam (HVA)</h3>
                <p class="title">Frontend Design and Development</p>
                <p class="date">sep. 2022 - jul. 2024</p>
            </div>
        </div>
        <div id="school2">
            <div class="info">
                <h3>Windesheim Almere</h3>
                <p class="title">Software Development</p>
                <p class="date">sep. 2020 - jul. 2022</p>
            </div>
        </div>
        <div id="school3">
            <div class="info">
                <h3>ROC Flevoland Almere Buiten</h3>
                <p class="title">ICT- & Netwerkbeheer</p>
                <p class="date">sep. 2017 - jul. 2020</p>
            </div>
        </div>
        <div id="school4">
            <div class="info">
                <h3>OSG de Meergronden</h3>
                <p class="title">HAVO (Natuur en Gezondheid)</p>
                <p class="date">sep. 2013 - jul. 2017</p>
            </div>
        </div>
        <div id="school5">
            <div class="info">
                <h3>OBS de Wierwinde</h3>
                <p class="title">HAVO/VWO advies behaald</p>
                <p class="date">sep. 2005 - jul. 2013</p>
            </div>
        </div>
    </div>
</section>
<section id="section4">
    <div id="contact">
        <h3 id="contacttitle">contact</h3>
        <div>
            <img src={PhoneLogo} alt="phone logo">
            <p>0637281639</p>
        </div>
        <div>
            <img src={MailLogo} alt="mail logo">
            <p>trisjanm@hotmail.com</p>
        </div>
        <div>
            <img src={LocationLogo} alt="location logo">
            <p>almere</p>
        </div>
    </div>
    <div id="skills">
        <h3 id="skillstitle">skills</h3>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>figma</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>html</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>css</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>javascript</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>github</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>sveltekit</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>content management system (cms)</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>english</p>
        </div>
        <div>
            <img src={BulletPolygon} alt="bulletpoint">
            <p>nederlands</p>
        </div>
    </div>
    <div id="hobbys">
        <h3 id="hobbystitle">hobbys</h3>
        <div>
            <img src={CameraLogo} alt="camera logo">
            <p>fotografie</p>
        </div>
        <div>
            <img src={SportsLogo} alt="sports logo">
            <p>sporten</p>
        </div>
        <div>
            <img src={GameLogo} alt="game logo">
            <p>gamen</p>
        </div>
    </div>
</section>

<style>
    section {
        display: flex;
        gap: 5rem;
        
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
    }

    section {
        min-height: 100vh;
        width: 100%;
    }
    
    section:nth-of-type(even) {
        background-color: var(--secondary-light-color);
    }

    #abouttext {
        font-size: 1.2em;
    }

    #section1 {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    #section1 p {
        max-width: 65vw;
    }

    #section2 {
        flex-direction: column;
        gap: 0;
        padding: 5rem 5rem;
    }

    #section2 .jobs div {
        min-height: 50vh;
        display: flex;
    }

    #section2 .jobs div .logo {
        width: 20vw;
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }

    #section2 .jobs div .logo img {
        height: 20vh;
        clip-path: circle(50% at 50% 50%);
        padding: 0;
        margin: 0;
    }

    #section2 .jobs div .info {
        flex-direction: column;
        justify-content: center;
        width: 70%;
    }

    #section2 .jobs div .info .title {
        font-weight: 500;
        font-size: 1.5rem;
    }

    #section2 .jobs div .info .description {
        font-weight: 400;
        font-size: 1.2rem;
    }

    #section2 .jobs div .info .date {
        font-weight: 300;
        font-size: 1rem;
    }

    #section3 {
        gap: 0;
        /* padding: 5rem 5rem; */
    }

    #section3 .section_title img {
        width: 70%;
    }

    #section3 .education div {
        padding: 0.3rem 0rem;
    }

    #section4 {
        display: flex;
        align-items: flex-start;
    }

    #section4 > div {
        margin: 30vh 0;
    }

    #section4 > div > div {
        display: flex;
        padding: 0.5rem 0;
        gap: 1rem;
    }

    #section4 > div > div img {
        width: 1.5rem;
    }

    #section4 > div > div p {
        font-size: 1.2rem;
    }
</style>