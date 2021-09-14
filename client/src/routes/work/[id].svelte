<script context="module">
    import { image_list } from "../../stores/images_api";
    
    export async function load({page}) {
        const id = page.params.id;
        /* TODO Loading error creates a memory hog */
        const image = image_list.find(image => image.id == id);

        return {
            props: { image }
        };
    }
</script>

<script>
    export let image;
    let {
        id,      /* For dynamic pages */
        src,     /* Image source */
        details, /* List of sources of detail images */
        title,
        size,
        price,
        dimensions,
        type
    } = image;
</script>

<div class="wrapper">
    <img src={src} alt="imgsrc" draggable="false">

    <div class="info">
        <h3>Title: {title}</h3>
        <h3>Size: {size}</h3>
        <!-- <h3>Price: ${price}</h3> -->
        <h3>Dimensions: {dimensions}</h3>
        <h3>Type: {type}</h3>
    </div>
</div>

<style>
    .wrapper {
        display: flex;
        /* gap: 1.5rem; */
        margin: 4.5rem auto 1rem auto;
        width: 100%;
        align-items: center;
        padding-left: 1rem;
    }

    .info {
        display: flex;
        flex-direction: column;
    }

    .info h3 {
        margin-left: 1rem;
        font-size: 3rem;
    }

    img {
        width: 27%;
        border-radius: 4px;
        box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.25),
            0 0 0.5em 0 var(--border-color);
        outline: 0;
        overflow: hidden;
    }

    @media (max-width: 1280px) {
        img {
            width: 35%;
        }
    }

    @media (max-width: 1024px) {
        img {
            width: 55%;
        }
    }

    @media (max-width: 769px) {
        img {
            width: 75%;
        }
    }

    @media (max-width: 480px) {
        img {
            width: 95%;
        }
    }
</style>
