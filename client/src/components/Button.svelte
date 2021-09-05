<button class="
    flex
    gap-2
    items-center
    font-light
    py-2 px-4
    rounded-md
    hover:bg-yellow-300
    hover:border-gray-400
    border-gray-100
">
    <slot></slot>
</button>

<style>
    button {
        box-shadow: 0 2px 5px 0 rgba(24, 24, 24, 0.12),
            0 2px 10px 0 rgba(24, 24, 24, 0.12);
        border-width: 1px;
        /* border-color: #e0e0e0; */
    }
</style>
