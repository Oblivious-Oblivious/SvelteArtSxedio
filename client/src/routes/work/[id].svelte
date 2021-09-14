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

<div>
    id: {id} <br>
    src: {src} <br>
    details: {details} <br>
    title: {title} <br>
    size: {size} <br>
    price: {price} <br>
    dimensions: {dimensions} <br>
    type: {type} <br>
</div>

<style>
    div {
        margin-top: 5rem;
    }
</style>
