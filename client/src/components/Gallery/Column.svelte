<script>
    import GalleryGard from "./GalleryCard.svelte";

    export let image_list;
</script>

<div>
    {#each image_list as image}
        <GalleryGard {image}/>
    {/each}
</div>
