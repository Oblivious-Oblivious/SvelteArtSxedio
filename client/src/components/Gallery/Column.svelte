<script>
    import PictureCard from "./PictureCard.svelte";

    export let image_list;
</script>

<div>
    {#each image_list as image}
        <PictureCard image_details={image}/>
    {/each}
</div>
