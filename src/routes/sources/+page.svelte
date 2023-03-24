<script>
    import Header from '$lib/Header.svelte';
    import Source from  '$lib/Source.svelte';
    import Footer from  '$lib/Footer.svelte';
    import '../../styles/Source.scss';
    import * as sources_data from '../../data/sources_data.json';
</script>

<Header title="Section 14" subtitle="Rights of the Accused" />

<div class="nav-background"></div>

<main>
    <section class="sources">
        {#each sources_data.sources as source}
            <Source index={sources_data.sources.indexOf(source)} />
        {/each}
    </section>
    
    <Footer />
</main>
