<script>
    import { underline_value } from "../../stores/underline_value";

    let u1 = false;
    let u2 = false;
    let u3 = false;
    let u4 = false;

    $: {
        switch($underline_value) {
            case 1: u1 = true; u2 = false;  u3 = false; u4 = false; break;
            case 2: u1 = false; u2 = true; u3 = false; u4 = false; break;
            case 3: u1 = false; u2 = false; u3 = true; u4 = false; break;
            case 4: u1 = false; u2 = false; u3 = false; u4 = true; break;
            default: u1 = false; u2 = false; u3 = false; u4 = false; break;
        }
    }
</script>

<ul>
    <li>
        <a class:u1 href="/">Home</a>
    </li>
    <li>
        <a class:u2 href="/gallery">Gallery</a>
    </li>
    <li>
        <a class:u3 href="/shop">Shop</a>
    </li>
    <li>
        <a class:u4 href="/about">About</a>
    </li>
</ul>

<style>
    ul {
        display: flex;
        gap: 2.85rem;
    }

    a {
        font-weight: 300;
        display: flex;
        position: relative;
        width: fit-content;
        margin: 0 0.3rem;
        padding: 0.2em 0;
    }

    /* Fade in */
    a::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 1px;
        background-color: var(--underline-color);
        overflow: hidden;
        transition: opacity 400ms, transform 400ms;

        opacity: 0;
        transform: translate3d(-100%, 0, 0);
    }

    /* Slide in */
    a:hover::after,
    a:focus::after {
        opacity: 1;
        transform: translate3d(0, 0, 0);
    }

    .u1:after, .u2:after, .u3:after, .u4:after {
        opacity: 1;
        transform: translate3d(0, 0, 0);
    }
</style>
