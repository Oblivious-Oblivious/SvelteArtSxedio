<script>
    import ContactDetail from "./ContactDetail.svelte";
</script>

<div class="contact">
    <div>
        <ContactDetail
            icon="fa fa-map-marker"
            text="Raidestou 18 - Serres, Greece"
        />
    </div>
    <div>
        <ContactDetail
            icon="fa fa-phone"
            text="+30 6946550215"
        />
    </div>
    <a style="color: #5383d3;" href="mailto:evang.papap@gmail.com" draggable="false">
        <ContactDetail
            icon="fa fa-envelope"
            text="evang.papap@gmail.com"
        />
    </a>
</div>

<style>
    .contact {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
    }
</style>
