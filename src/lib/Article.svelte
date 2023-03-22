<script>
    import '../styles/Article.scss';
    import * as article_data from '../data/article_data.json';
    import { active_article } from '../stores.js';

    let index;

    active_article.subscribe(value => {
        index = value;
    });
</script>

<section class="content" id="content">
    <figure><img src={article_data.articles[index].infographic}></figure>   

    <article>
        <h2>{article_data.articles[index].title}</h2>
        {@html article_data.articles[index].text}
    </article>
</section>
