<script>
    import Lightbox from "../Lightbox.svelte";

    export let image;
    let [image_source, image_caption] = image;

    let lightbox_is_visible = false;
    const toggle_visibility = () =>
        lightbox_is_visible = !lightbox_is_visible;
</script>

<div on:click={toggle_visibility} class="thumbnail" draggable="false">
    <img src={image_source} alt="imgsrc" draggable="false">
    <h3>{image_caption}</h3>
</div>

{#if lightbox_is_visible}
    <Lightbox
        on:click={toggle_visibility}
        {image_source}
    />
{/if}

<style>
    img {
        cursor: pointer;
        width: 100%;
    }

    h3 {
        color: var(--text-color);
        font-weight: 300;
        line-height: 1.5;
        margin: 1rem 0 1rem 0;
        font-size: 1rem;
    }

    .thumbnail {
        border-bottom: none;
        display: block;
        width: 100%;
        margin: 0 0 2rem 0;
        text-align: center;
        border-radius: 4px;
        box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.25),
            0 0 0.5em 0 var(--border-color);
        background-color: rgba(255, 255, 255, 0.075);
        cursor: pointer;
        outline: 0;
        overflow: hidden;
        transition: all 200ms ease;
    }

    .thumbnail img {
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
    }

    .thumbnail:hover {
        background-color: rgba(255, 255, 255, 0.25);
        box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.25),
            0 0 0.5em 0 var(--yellow);
    }
</style>
