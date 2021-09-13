<script>
    import { fade } from "svelte/transition";

    export let image_details;

    let is_visible = false;
    const toggle_visibility = () =>
        is_visible = !is_visible;
</script>

<div on:click={toggle_visibility} class="thumbnail" draggable="false">
    <img src={image_details[0]} alt="imgsrc" draggable="false">
    <h3>{image_details[1]}</h3>
</div>

{#if is_visible}
    <div
        transition:fade
        on:click={toggle_visibility}
        class="lightbox lightbox-img lightbox-visible"
    >
        <div class="lightbox-placeholder" role="dialog">
            <img src={image_details[0]} alt="imgsrc" draggable="false">
        </div>
    </div>
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

    .lightbox {
        position: fixed;
        display: flex;
        justify-content: center;
        align-items: center;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        
        box-sizing: content-box;
        background: rgba(0, 0, 0, 0.75);
        overflow: hidden;

        opacity: 0.01;
        transition: opacity 400ms ease;
        z-index: 1000;
        will-change: opacity;
    }

    .lightbox-visible {
        opacity: 1;
    }

    .lightbox-placeholder {
        max-width: 100%;
        transform: scale(0.9);
        transition: transform 400ms ease;
        z-index: 1;
        will-change: transform;
    }

    .lightbox-placeholder img:first-child:last-child {
        display: block;
        position: absolute;

        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        margin: auto;

        width: auto;
        height: auto;
        max-width: 87.5%;
        max-height: 87.5%;

        border-radius: 4px;
        box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.25),
            0 0 0.5em 0 var(--white-color);
    }

    .lightbox-img .lightbox-placeholder {
        width: 100%;
        height: 100%;
        pointer-events: none;
    }

    .lightbox-visible .lightbox-placeholder {
        transform: scale(1);
    }
</style>
