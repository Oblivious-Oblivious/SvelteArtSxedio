<script>
    import Copyright from "./Copyright.svelte";
    import Contact from "./Contact.svelte";
</script>

<footer class="grid md:grid-cols-2 items-center p-8 footer-has-shadow">
    <div class="col-span-3 md:col-span-1">
        <Copyright/>
    </div>

    <hr class="md:hidden py-3 col-span-3 text-gray-300 opacity-50">

    <div class="col-span-3 md:col-span-1">
        <Contact/>
    </div>
</footer>

<style>
    .footer-has-shadow {
        box-shadow: 0 -2px 5px 0 rgba(24, 24, 24, 0.12),
            0 2px 10px 0 rgba(24, 24, 24, 0.12);
    }
</style>
