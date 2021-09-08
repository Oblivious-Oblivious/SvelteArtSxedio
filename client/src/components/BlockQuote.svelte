<script>
    export let cite = "";
</script>

<div class="quote">
    <!-- TODO Fix blockquote overflow -->
    <blockquote>
        <slot></slot>
    </blockquote>
    <cite> {cite} </cite>
</div>

<style>
    .quote {
        display: grid;
        justify-content: center;
        color: var(--text-color);
        background-color: var(--body-bg-color);
        margin: 4rem;
    }

    cite {
        display: grid;
        justify-content: flex-end;
        font-weight: 100;
        font-size: 2rem;
        font-style: italic;
        line-height: 2.5;
        text-align: left;
    }

    blockquote {
        font-weight: 100;
        font-size: 2rem;
        font-style: italic;
        max-width: 600px;
        line-height: 1.4;
        margin: 8rem 0 auto;
        padding: 1rem;
    }

    blockquote:before,
    blockquote:after {
        position: absolute;
        color: var(--underline-color);
        font-size: 8rem;
        width: 4rem;
        height: 4rem;
    }

    blockquote:before {
        content: '“';
        top: 9.5rem;
        left: 23.5rem;
    }

    blockquote:after {
        content: '”';
        top: 14.5rem;
        right: 36rem;
    }
</style>
