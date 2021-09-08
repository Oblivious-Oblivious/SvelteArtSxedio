<div class="container">
    <div class="content">
        <slot></slot>
    </div>
</div>

<style>
    .container {
        font-family: var(--font);
        margin: 0 auto;
        background: var(--body-bg-color);
        box-shadow: 5px 5px 15px var(--shadow-color);
        border-radius: 10px;
    }

    .content {
        color: var(--text-color);
        font-size: 1.25rem;
        font-weight: 300;
        text-align: center;
        padding: 1.25rem;
        margin: 2rem 0;
    }
</style>
