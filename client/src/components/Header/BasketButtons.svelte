<script>
    import Button from "../Button.svelte";

    $: price = (0.00).toFixed(2);
    $: number_of_items = 0;

    const toggle_theme = () => {
        /* TODO Toggle theme */
    }

    const preload_basket = () => {
    }
</script>

<Button on:click={toggle_theme}><i class="fad fa-paint-brush"></i></Button>

<a href="/basket">
    <Button on:click={preload_basket}>
        <i class="fas fa-shopping-cart"></i>
        <div>
            {`$${price}`}
        </div>
        <div>
            {`(${number_of_items})`}
        </div>
    </Button>
</a>

<style>
    /* TODO Turn into global */
    @import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.9.0/css/all.css");

    i {
        font-family: "Font Awesome 5 Free";
    }
</style>
