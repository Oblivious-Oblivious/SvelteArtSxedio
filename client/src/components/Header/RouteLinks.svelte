<ul>
    <li>
        <a href="/">Home</a>
    </li>
    <li>
        <a href="/gallery">Gallery</a>
    </li>
    <li>
        <a href="/shop">Shop</a>
    </li>
    <li>
        <a href="/about">About</a>
    </li>
</ul>

<style>
    ul {
        display: flex;
        gap: 2.85rem;
    }

    a {
        font-weight: 300;
        position: relative;
        padding: 0.2rem 0.3rem;
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
