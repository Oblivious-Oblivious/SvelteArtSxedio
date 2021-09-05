<script>
    import Logo from "./Logo.svelte";
    import Burger from "./Burger.svelte";
    import RouteLinks from "./RouteLinks.svelte";
    import BasketButtons from "./BasketButtons.svelte";
</script>

<header>
    <nav class="logo">
        <Logo/>
    </nav>

    <nav class="route-links">
        <RouteLinks/>
    </nav>

    <nav class="basket-buttons">
        <BasketButtons/>
    </nav>

    <!-- Shown on medium and below -->
    <nav class="burger">
        <Burger/>
    </nav>
</header>

<style>
    header {
        position: fixed;
        width: 100%;
        box-shadow: 0 2px 5px 0 rgba(24, 24, 24, 0.12),
            0 2px 10px 0 rgba(24, 24, 24, 0.12);
        padding: 0.5rem 0.875rem;
        display: flex;
        justify-content: space-between;
    }

    .logo {
        width: 12rem;
        padding: 0 2.25rem;
        display: flex;
        align-items: center;
    }

    .route-links {
        display: none;
    }
    
    .basket-buttons {
        display: none;
    }

    .burger {
        display: flex;
        align-items: flex-end;
        justify-content: flex-end;
    }

    /* TODO Use aero css flexbox automations */
    @media (min-width: 768px) {
        .route-links {
            display: flex;
            align-items: center;
            gap: 3.5rem;
            padding: 0 1rem;
            justify-content: flex-end;
            width: 100%;
        }

        .basket-buttons {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0 2rem;
        }

        .burger {
            display: none;
        }
    }
</style>
