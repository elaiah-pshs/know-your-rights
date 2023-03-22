<script>
    import '../styles/Deck.scss';
    import Card from '$lib/Card.svelte';
    import * as card_data from '../data/card_data.json';
</script>

<section class="deck">
    {#each card_data.cards as card}
        <Card index={card_data.cards.indexOf(card)} />
    {/each}
</section>
