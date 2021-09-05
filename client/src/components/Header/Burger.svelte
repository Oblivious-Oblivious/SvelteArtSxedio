<script>
    let open = false;

    const x2_line1picker = {false: 66, true: 70};
    const x2_line2picker = {false: 54, true: 70};
    const x2_line3picker = {false: 42, true: 70};
</script>

<!-- TODO Figure out svg on hover effects -->
<!-- on:hover={expand_burger} -->

<button
    class:open
    class="burger"
    on:click={() => open = !open}
>
    <svg width="40px" height="40px" viewBox="0 0 72 72">
        <g id="line">
            <line id="top" x1="16" x2={x2_line1picker[open]} y1="26" y2="26"/>
            <line id="mid" x1="16" x2={x2_line2picker[open]} y1="36" y2="36"/>
            <line id="bot" x1="16" x2={x2_line3picker[open]} y1="46" y2="46"/>
        </g>
    </svg>
</button>

<style>
    .burger {
        padding: 0.25rem 0.75rem;
        transition: color 0.3s ease-in-out;
    }

    #top, #mid, #bot {
        stroke: #4e4e4e;
        stroke-linecap: round;
        stroke-linejoin: round;
        stroke-miterlimit: 10;
        stroke-width: 2;
        fill: none;
        transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
    }

    /* rotate the top line */
    .open #top {
        transform: translate(30px, -10px) rotate(44deg);
    }

    /* hide the middle */
    .open #mid {
        opacity: 0
    }

    /* rotate the bottom line */
    .open #bot {
        transform: translate(-20px, 34px) rotate(-43deg)
    }
</style>
