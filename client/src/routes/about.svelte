<script>
    import { onMount } from "svelte";
    import { underline_value } from "../stores/underline_value";

    onMount(() => $underline_value = 4);
</script>

<h1>About</h1>

<style>
    h1 {
        text-align: center;
        font-size: 2.5rem;
        padding: 40rem 20rem;
    }
</style>
