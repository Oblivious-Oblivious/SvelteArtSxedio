<!-- <script context="module">
    import { browser, dev } from "$app/env";
    export const hydrate = dev;
    export const router = browser;
    export const prerender = true;
</script> -->

<script>
    import { onMount } from "svelte";
    import { underline_value } from "../stores/underline_value";

    import Column from "../components/Gallery/Column.svelte";
    
    onMount(() => $underline_value = 2);
    
    let image_list1 = [
        ["img/tall/Rose.jpg", "Rose"],
        ["img/wide/River Boat.jpg", "River Boat"],
        ["img/wide/Fruit.jpg", "Fruit"],
        ["img/tall/Poppies.jpg", "Poppies"],
        ["img/wide/Leaves.jpg", "Leaves"]
    ];
    let image_list2 = [
        ["img/ultra-wide/details/Pumkin detail1.jpg", "Pumkin"],
        ["img/wide/Waves.jpg", "Waves"],
        ["img/wide/Rocks.jpg", "Rocks"],
        ["img/tall/River.jpg", "River"],
        ["img/tall/Salt Shaker.jpg", "Salt Shacker"]
    ];
    let image_list3 = [
        ["img/tall/Ver Meer.jpg", "Ver Meer"],
        ["img/tall/Dali.jpg", "Dali"],
        ["img/wide/Peaches.jpg", "Peaches"],
        ["img/tall/Pencil.jpg", "Pencil"],
        ["img/ultra-wide/Naxos.jpg", "Naxos"]
    ];
</script>

<div class="image-grid">
    <div class="image-col"><Column image_list={image_list1}/></div>
    <div class="image-col"><Column image_list={image_list2}/></div>
    <div class="image-col"><Column image_list={image_list3}/></div>
</div>

<style>
    .image-grid {
        padding-top: 4.5rem;
        display: flex;
        justify-content: center;
    }

    .image-col {
        display: flex;
        flex-direction: column;
        width: 24%;
        padding: 0 1rem;
    }

    @media (max-width: 1024px) {
        .image-grid {
            padding-top: 5rem;
            display: flex;
            flex-direction: column;
        }

        .image-col {
            width: 50%;
            margin: 0 auto;
            padding: 0 1rem;
        }
    }

    @media (max-width: 769px) {
        .image-col {
            width: 75%;
        }
    }
</style>
