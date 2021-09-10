<script context="module">
    // import image_list from "../../stores/images_api";

    export async function load({page}) {
        const id = page.params.id;
        const image = `id: ${id}`;

        return {
            props: {image}
        };
    }
</script>

<!-- TODO Fix reloading error when going from image id to gallery -->
<script>
    import { onMount } from "svelte";
    import { underline_value } from "../../stores/underline_value";

    onMount(() => $underline_value = 0);

    export let image;
</script>

<h2>{image}</h2>

<style>
    h2 {
        font-size: 2rem;
        margin: 4rem auto;
    }
</style>
