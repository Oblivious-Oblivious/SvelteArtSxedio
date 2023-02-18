<script>
    export let text;
    export let icon;
</script>


<i class={icon}></i>
&nbsp;
{text}

<style>
    @import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.9.0/css/all.css");

    i {
        font-family: "Font Awesome 5 Free";
        background-color: var(--underline-color);
        color: var(--white-color);
        font-size: 18px;
        width: 38px;
        height: 38px;
        border-radius: 50%;
        text-align: center;
        line-height: 38px;
    }
</style>
