<script>

	import { each } from "svelte/internal";

</script>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<h1>real_sirlije</h1>

{#each Array(3) as _, i}
    <li>{i + 1}</li>
{/each}

