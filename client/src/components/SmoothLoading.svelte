<script>
    import { blur } from "../animations/blur";

    export let refresh = "";
</script>

{#key refresh}
    <div transition:blur>
        <slot/>
    </div>
{/key}
