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
        box-shadow: 0 2px 5px 0 var(--nav-shadow-color),
            0 2px 10px 0 var(--nav-shadow-color);
        border-width: 1px;

        color: var(--dark-color);
        background-color: var(--button-bg-color);
        border-color: #dbdbdb;
    }

    button:hover {
        color: var(--dark-color);
        background-color: var(--yellow);
        border-color: #b5b5b5;
    }
</style>
