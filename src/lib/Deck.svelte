<script>
    import '../styles/Deck.scss';
    import Card from '$lib/Card.svelte';
    import * as article_data from '../data/article_data.json';
</script>

<section class="deck">
    {#each article_data.articles as card}
        <Card index={article_data.articles.indexOf(card)} />
    {/each}
</section>
