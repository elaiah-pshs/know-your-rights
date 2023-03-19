<script>
    import '../styles/Deck.scss';
    import Card from '$lib/Card.svelte';
    import * as card_data from '../data/card_data.json';
</script>

<section class="deck">
    <Card header={true} icon="../images/12.png" />
    {#each card_data.cards as card}
        <Card header={false} icon={card.icon} number={card.number} title={card.title} figure={card.figure} />
    {/each}
</section>
