<script>
    import { onMount } from "svelte";
    import { underline_value } from "../stores/underline_value";

    import Column from "../components/Gallery/Column.svelte";
    
    onMount(() => $underline_value = 2);
    
    let image_list1 = [
        ["img/tall/Rose.JPG", "Rose"],
        ["img/wide/River Boat.JPG", "River Boat"],
        ["img/wide/Fruit.JPG", "Fruit"],
        ["img/tall/Poppies.JPG", "Poppies"],
        ["img/wide/Leaves.JPG", "Leaves"]
    ];
    let image_list2 = [
        ["img/ultra-wide/details/Pumkin detail1.JPG", "Pumkin"],
        ["img/wide/Waves.JPG", "Waves"],
        ["img/wide/Rocks.JPG", "Rocks"],
        ["img/tall/River.JPG", "River"],
        ["img/tall/Salt Shaker.JPG", "Salt Shacker"]
    ];
    let image_list3 = [
        ["img/tall/Ver Meer.JPG", "Ver Meer"],
        ["img/tall/Dali.JPG", "Dali"],
        ["img/wide/Peaches.JPG", "Peaches"],
        ["img/tall/Pencil.JPG", "Pencil"],
        ["img/ultra-wide/Naxos.JPG", "Naxos"]
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
