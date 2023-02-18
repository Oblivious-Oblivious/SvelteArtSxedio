<script>
    import Logo from "./Logo.svelte";
    import Burger from "./Burger.svelte";
    import RouteLinks from "./RouteLinks.svelte";
    import MobileRouteLinks from "./MobileRouteLinks.svelte";

    let open = false;

    const burger_open_handler = e => open = e.detail.status;
    const close_burger_menu = () => open = false;
</script>

<header class:open>
    <nav class="logo">
        <Logo/>
    </nav>

    <nav class="route-links">
        <RouteLinks/>
    </nav>

    <!-- Shown on medium and below -->
    <nav class="burger">
        <Burger
            {open}
            on:burger-open={burger_open_handler}
        />
    </nav>
</header>

<div
    class:open
    class="mobile-nav"
>
    <MobileRouteLinks
        on:click={close_burger_menu}
    />
</div>

<style>
    header {
        position: fixed;
        background-color: var(--nav-bg-color);
        top: 0;
        left: 0;
        width: 100vw;
        box-shadow: 0 2px 5px 0 var(--nav-shadow-color),
            0 2px 10px 0 var(--nav-shadow-color);
        padding: 0.75rem 2rem;
        display: flex;
        justify-content: space-between;
    }

    header.open {
        box-shadow: none;
        transition: 300ms;
    }

    .logo {
        width: 12rem;
        padding: 0 2.25rem;
        display: flex;
        align-items: center;
    }

    .route-links {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        width: 100%;
        padding: 0 2.3rem;
    }

    .burger {
        display: none;
    }

    @media (max-width: 1024px) {
        .route-links {
            display: none;
        }

        .burger {
            position: relative;
            display: flex;
            align-items: flex-end;
            justify-content: flex-end;
        }
    }

    .mobile-nav {
        position: fixed;
        top: 3.9rem;
        left: 100%;
        width: 100%;
        min-height: max-content;
        display: block;
        z-index: 98;
        box-shadow: 0 2px 5px 0 var(--nav-shadow-color);
        background-color: var(--nav-bg-color);
        transition: 300ms;
    }

    .mobile-nav.open {
        left: 0%;
    }
</style>
