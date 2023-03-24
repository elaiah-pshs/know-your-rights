<script>
    export let index;
    import '../styles/Card.scss';
    import * as article_data from '../data/article_data.json';
    import { active_article } from '../stores.js';

    function changeArticle() {
        active_article.update(n => index);
    }
</script>

{#if index == 0}
    <a href="#content" class="card slot" on:click={changeArticle}>
        <div class="card-header">
            <img src="../icons/favicon.png">
            <svg viewBox="0 0 106 57">
                <path d="M102 4c0 27.1-21.9 49-49 49S4 31.1 4 4"></path>
            </svg>

            <div class="card-header-text">
                <p>KNOW YOUR RIGHTS</p>
                <h2>Section 14</h2>
            </div>
        </div>
    </a>
{:else}
    <a href="#content" class="card normal" on:click={changeArticle}>
        <div class="card-header">
            <img src="../icons/favicon.png">
            <svg viewBox="0 0 106 57">
                <path d="M102 4c0 27.1-21.9 49-49 49S4 31.1 4 4"></path>
            </svg>

            <div class="card-header-text">
                <p>Part {index}:</p>
                <h2>{article_data.articles[index].title}</h2>
            </div>
        </div>

        <figure><img src={article_data.articles[index].infographic}></figure>
    </a>
{/if}
