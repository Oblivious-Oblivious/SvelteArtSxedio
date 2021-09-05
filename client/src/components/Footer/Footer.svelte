<script>
    import Copyright from "./Copyright.svelte";
    import Contact from "./Contact.svelte";
</script>

<footer>
    <div class="copyright">
        <Copyright/>
    </div>

    <hr class="divider">

    <div class="contact">
        <Contact/>
    </div>
</footer>

<style>
    footer {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        align-items: center;
        padding: 2rem;
        font-weight: 300;
        box-shadow: 0 -2px 5px 0 rgba(24, 24, 24, 0.12),
            0 2px 10px 0 rgba(24, 24, 24, 0.12);
    }
    .copyright, .contact {
        grid-column: span 3 / span 3;
    }

    .divider {
        padding: 0.75rem 0;
        grid-column: span 3 / span 3;
        color: rgba(152, 152, 152, 0.3);
    }

    /* TODO Use custom aero flexbox automations */
    @media (min-width: 768px) {
        .copyright, .contact {
            grid-column: span 1 / span 1;
        }

        .divider {
            display: none;
        }
    }
</style>
