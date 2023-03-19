<script>
    import '../styles/Card.scss';
    export let header, icon, number, title, figure;
</script>

{#if header}
    <header class="card">
        <img src={icon}>
        <svg viewBox="0 0 106 57">
            <path d="M102 4c0 27.1-21.9 49-49 49S4 31.1 4 4"></path>
        </svg>

        <div>
            <p>KNOW YOUR RIGHTS</p>
            <h2>Section 14</h2>
        </div>
    </header>
{:else}
    <a class="card" href="#section-1">
        <header class="card-header">
            <img src={icon}>
            <svg viewBox="0 0 106 57">
                <path d="M102 4c0 27.1-21.9 49-49 49S4 31.1 4 4"></path>
            </svg>

            <div>
                <p>Section {number}:</p>
                <h2>{title}</h2>
            </div>
        </header>

        <figure><img src={figure}></figure>
    </a>
{/if}
