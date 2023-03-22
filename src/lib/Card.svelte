<script>
    import '../styles/Card.scss';
    export let slot, icon, number, title, figure;
</script>

{#if slot}
    <div class="card slot">
        <div class="card-header">
            <img src={icon}>
            <svg viewBox="0 0 106 57">
                <path d="M102 4c0 27.1-21.9 49-49 49S4 31.1 4 4"></path>
            </svg>

            <div class="card-header-text">
                <p>KNOW YOUR RIGHTS</p>
                <h2>Section 14</h2>
            </div>
        </div>
    </div>
{:else}
    <div class="card normal">
        <div class="card-header">
            <img src={icon}>
            <svg viewBox="0 0 106 57">
                <path d="M102 4c0 27.1-21.9 49-49 49S4 31.1 4 4"></path>
            </svg>

            <div class="card-header-text">
                <p>Section {number}:</p>
                <h2>{title}</h2>
            </div>
        </div>

        <figure><img src={figure}></figure>
    </div>
{/if}
