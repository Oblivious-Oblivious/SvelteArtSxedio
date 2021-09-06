<ul>
    <li on:click>
        <a href="/">Home</a>
    </li>
    <li on:click>
        <a href="/gallery">Gallery</a>
    </li>
    <li on:click>
        <a href="/shop">Shop</a>
    </li>
    <li on:click>
        <a href="/about">About</a>
    </li>
</ul>

<style>
    ul {
        display: flex;
        flex-direction: column;
    }

    a {
        font-weight: 300;
        display: flex;
        position: relative;
        width: fit-content;
        margin: 0 auto;
        margin-top: 1rem;
        margin-bottom: 1rem;
        padding: 0.2em 0;
    }

    /* TODO Make underlines sticky */
    /* Fade in */
    a::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 1px;
        background-color: var(--underline-color);
        opacity: 0;
        transition: opacity 400ms, transform 400ms;
    }

    a:hover::after,
    a:focus::after {
        opacity: 1;
        transform: translate3d(0, 0.2em, 0);
    }

    /* Slide in */
    li a {
        overflow: hidden;
    }
    
    li a::after {
        opacity: 0;
        transform: translate3d(-100%, 0, 0);
    }

    li a:hover::after,
    li a:focus::after{
        transform: translate3d(0, 0, 0);
    }
</style>
