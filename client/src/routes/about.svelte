<script>
    import { onMount } from "svelte";
    import { underline_value } from "../stores/underline_value";

    import BlockQuote from "../components/BlockQuote.svelte";
    import Container from "../components/Container.svelte";

    onMount(() => $underline_value = 4);
</script>

<div class="about-container">
    <BlockQuote cite="&mdash;Vang 2019">
        On catefor up to the fanar, turn off
        engine and car tsouls down nicely.
    </BlockQuote>
    
    <img src="./img/about.jpg" alt="about" draggable="false"/>
    
    <Container>
        Super painter, sallonica arch dropout, because he alredy
        know these things, close to becoming OTE employee, has
        education as topograph at metsovo village.
        <br><br><br>
        Ah, he also makes karavaks.
    </Container>
</div>

<style>
    .about-container {
        width: 75%;
        margin: 0 auto;
    }

    img {
        width: 75%;
        margin: 0 auto;
        margin-top: 1rem;
        margin-bottom: 2rem;
        box-shadow: 5px 5px 15px var(--shadow-color);
        border-radius: 10px;
    }
</style>
