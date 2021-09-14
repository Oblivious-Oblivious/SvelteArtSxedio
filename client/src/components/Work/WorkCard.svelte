<script>
    export let image;
</script>

<!-- TODO Add a container for overlaying text on hover -->
<a href="/work/{image.id}">
    <img src="{image.src}" alt="imgsrc">
</a>

<style>
    a {
        border-bottom: none;
        display: block;
        width: 100%;
        text-align: center;
        border-radius: 4px;
        box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.25),
            0 0 0.5em 0 var(--border-color);
        background-color: rgba(255, 255, 255, 0.075);
        cursor: pointer;
        outline: 0;
        overflow: hidden;
    }

    /* TODO Blur only the image not the text */
    a:hover {
        filter: blur(4px);
        transition: all 400ms ease;
    }
</style>
