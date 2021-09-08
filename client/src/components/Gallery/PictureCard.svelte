<script>
    export let image_details;
</script>

<a href={image_details[0]} draggable="false">
    <img src={image_details[0]} alt="rose" draggable="false">
    <h3>{image_details[1]}</h3>
</a>

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

    a {
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

    a img {
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
    }

    a:hover {
        background-color: rgba(255, 255, 255, 0.25);
        box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.25),
            0 0 0.5em 0 var(--yellow);
    }
</style>
