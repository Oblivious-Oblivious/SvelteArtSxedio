<script>
    import ContactDetail from "./ContactDetail.svelte";
</script>

<div class="flex flex-col items-center justify-center text-center">
    <div>
        <ContactDetail
            icon="fa fa-map-marker"
            text="Raidestou 18 - Serres, Greece"
        />
    </div>
    <div class="phone-number-font">
        <ContactDetail
            icon="fa fa-phone"
            text="+30 6946550215"
        />
    </div>
    <a class="text-blue-500" href="mailto:evang.papap@gmail.com" draggable="false">
        <ContactDetail
            icon="fa fa-envelope"
            text="evang.papap@gmail.com"
        />
    </a>
</div>

<style>
    .phone-number-font {
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        font-weight: 300;
    }
</style>
