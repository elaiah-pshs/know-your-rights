<script>
    export let index;
    import '../styles/Source.scss';
    import * as sources_data from '../data/sources_data.json';
</script>

<p class="source">
    {sources_data.sources[index].author}
    
    {sources_data.sources[index].date}

    <i>
        {sources_data.sources[index].title}
    </i>

    {sources_data.sources[index].publisher}

    <br>

    <a href={sources_data.sources[index].link}>
        {sources_data.sources[index].link}
    </a>
</p>
