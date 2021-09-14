<script context="module">
    /* TODO Loading error creates a memory hog */
    import { image_list } from "../stores/images_api";

    export async function load() {
        return {
            props: {image_list}
        };
    }
</script>

<script>
    import { onMount } from "svelte";
    import { underline_value } from "../stores/underline_value";

    import WorkCard from "../components/Cards/WorkCard.svelte";

    onMount(() => $underline_value = 3);

    export let image_list;
</script>

<h1>My Work</h1>

<div class="wrapper">
    {#each image_list as image}
        <WorkCard {image}/>
    {/each}
</div>

<style>
    h1 {
        margin-top: 6.5rem;
        text-align: center;
        font-size: 4rem;
        font-style: italic;
    }

    .wrapper {
        display: grid;
        grid-template-columns: 23.4% 23.4% 23.4% 23.4%;
        gap: 1.5rem;
        margin: 4.5rem auto;
        width: 75%;
        align-items: center;
    }

    @media (max-width: 1280px) {
        .wrapper {
            grid-template-columns: 31.5% 31.5% 31.5%;
        }
    }

    @media (max-width: 1024px) {
        .wrapper {
            grid-template-columns: 47.5% 47.5%;
        }
    }

    @media (max-width: 769px) {
        .wrapper {
            grid-template-columns: 100%;
        }
    }
</style>
