<script>
    import "../resets.css";
    import "../variables.css";

    import Header from "../components/Header/Header.svelte";
    import Footer from "../components/Footer/Footer.svelte";
</script>

<!-- TODO Add smooth loading -->
<main>
    <Header/>
    <slot></slot>
    <Footer/>
</main>

<style>
    /* @import url("https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap"); */

    main {
        /* font-family: Raleway; */
        font-family: var(--font);
        font-feature-settings: "lnum"; /* Line-up number symbols */

        color: var(--text-color);
        background-color: var(--body-bg-color);
        background-image: var(--dark-bg);
        overflow: hidden;
        background-size: cover;
        background-position: top center;
    }
</style>
