<script>
    import ContactDetail from "./ContactDetail.svelte";
</script>

<div class="flex flex-col items-center justify-center text-center">
    <div>
        <ContactDetail
            icon="fa fa-map-marker footer-contacts-icon"
            text="Raidestou 18 - Serres, Greece"
        />
    </div>
    <div>
        <ContactDetail
            icon="fa fa-phone footer-contacts-icon"
            text="+30 6946550215"
        />
    </div>
    <a class="text-blue-500" href="mailto:evang.papap@gmail.com" draggable="false">
        <ContactDetail
            icon="fa fa-envelope footer-contacts-icon"
            text="evang.papap@gmail.com"
        />
    </a>
</div>
