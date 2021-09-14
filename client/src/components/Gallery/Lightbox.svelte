<script>
    import { fade } from "svelte/transition";

    export let image_source;
</script>

<div
    transition:fade
    on:click
    class="lightbox lightbox-img lightbox-visible"
>
    <div class="lightbox-placeholder" role="dialog">
        <img src={image_source} alt="imgsrc" draggable="false">
    </div>
</div>

<style>
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
