<script context="module">
    export async function load({page}) {
        return {
            props: {
                refresh: page.path
            }
        };
    }
</script>

<script>
    import "../styles/resets.css";
    import "../styles/variables.css";

    import Header from "../components/Header/Header.svelte";
    import Footer from "../components/Footer/Footer.svelte";

    import SmoothLoading from "../components/SmoothLoading.svelte";
    export let refresh;
</script>

<svelte:head>
    <style>
        body {
            font-family: var(--font);
            font-feature-settings: "lnum"; /* Line-up number symbols */

            color: var(--text-color);
            background-color: var(--body-bg-color);
            background-size: cover;
            background-position: top center;
        }
    </style>
</svelte:head>

<!-- TODO Add smooth loading -->

<main>
    <Header/>

    <SmoothLoading {refresh}>
        <slot></slot>
    </SmoothLoading>

    <Footer/>
</main>
