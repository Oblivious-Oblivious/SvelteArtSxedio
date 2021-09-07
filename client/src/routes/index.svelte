<script>
    import { onMount } from "svelte";
    import { underline_value } from "../stores/underline_value";

    onMount(() => $underline_value = 1);
</script>

<h1>Here the good pepons (drawn).</h1>

<style>
    h1 {
        font-weight: 300;
        text-align: center;
        font-size: 2.5rem;
        padding: 40rem 20rem;
    }
</style>
