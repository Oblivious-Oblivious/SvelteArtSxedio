<script>
    import Logo from "./Logo.svelte";
    import Burger from "./Burger.svelte";
    import RouteLinks from "./RouteLinks.svelte";
    import BasketButtons from "./BasketButtons.svelte";
</script>

<header class="fixed w-full shadow-lg px-3.5 py-2 flex justify-between">
    <nav class="w-44 px-9 flex items-center">
        <Logo/>
    </nav>

    <nav class="hidden md:flex md:items-center gap-14 px-4 justify-end w-full">
        <RouteLinks/>
    </nav>

    <nav class="hidden md:flex md:items-center gap-2 px-8">
        <BasketButtons/>
    </nav>

    <!-- Shown on medium and below -->
    <nav class="flex items-end justify-end md:hidden">
        <Burger/>
    </nav>
</header>
