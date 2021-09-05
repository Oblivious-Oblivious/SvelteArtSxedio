<button>
    <slot></slot>
</button>

<style>
    button {
        display: flex;
        gap: 0.5rem;
        align-items: center;
        font-weight: 300;
        padding: 0.5rem 1rem;
        border-radius: 0.375rem;
        box-shadow: 0 2px 5px 0 rgba(24, 24, 24, 0.12),
            0 2px 10px 0 rgba(24, 24, 24, 0.12);
        border-width: 1px;
        border-color: #e0e0e0;
    }

    button:hover {
        color: #4e4e4e;
        background-color: #fedd56;
        border-color: rgb(152, 152, 152);
    }
</style>
