<script>
    import Copyright from "./Copyright.svelte";
    import Contact from "./Contact.svelte";
</script>

<footer class="footer-has-shadow flex items-center justify-center p-10">
    <div class="w-1/2">
        <Copyright/>
    </div>

    <div class="w-1/2">
        <Contact/>
    </div>
</footer>

<style>
    .footer-has-shadow {
        box-shadow: 0 -2px 5px 0 rgba(24, 24, 24, 0.12),
            0 2px 10px 0 rgba(24, 24, 24, 0.12);
    }
</style>
