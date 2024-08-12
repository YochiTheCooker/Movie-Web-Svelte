<script>
 export let  title, year, poster
</script>

<article>
    <h2>{title}</h2>
    <h4>{year}</h4>
    <img alt={title} src={poster}/>
</article>

<style>
    article {
        border: 1px solid #eee;
        border-radius: 4px;
        margin-bottom: 8px; padding: 16px;
        text-align: center;
    }
    h2 {
    font-size: 24px;
    margin-bottom: 4px;
    }
</style>


