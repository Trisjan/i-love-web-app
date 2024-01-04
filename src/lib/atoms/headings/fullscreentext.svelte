<script>
    export let text;
</script>

<p>{text}</p>

<style>
    p {
        font-family: 'Raleway', sans-serif;
        font-weight: bold;
        text-transform: uppercase;
        font-size: calc(var(--font-scale) * 3 * var(--font-size));
    }

    /* // Medium devices (tablets, 768px and up) */
    @media (min-width: 768px) { 
        p {
            font-size: calc(var(--font-scale) * 6 * var(--font-size));
        }
    }

    /* // Large devices (desktops, 992px and up) */
    @media (min-width: 992px) {
        p {
            font-size: calc(var(--font-scale) * 8 * var(--font-size));
        }
    }

    /* // X-Large devices (large desktops, 1200px and up) */
    @media (min-width: 1200px) { 
        p {
            font-size: calc(var(--font-scale) * 8 * var(--font-size));
        }
    }

</style>