<script>
import Movie from "./Movie.svelte"
let value = ''

const handleInput = (e) => value = e.target.value;
let response = []

$: if (value.length > 2) {
    
    response = fetch(`https://www.omdbapi.com/?s=${value}&apikey=7526bda3`)
    .then(res => res.json())
    .then(apiResponse =>  apiResponse.Search || [])
}
</script>

<input placeholder="Buscando peliculas..." {value} on:input={handleInput}> 

{#await response}
    <div class= "spinner"> </div>
{:then movies} 
    {#each movies as {Title, Year, Poster}}
    <Movie
        title={Title}
        year={Year}
        poster={Poster}
      />
    {:else}
    <strong>No hay resultados!</strong>
    {/each}
{/await}


<style>
    .spinner{
        border: 4px solid rgba(0,0,0, .1);
        width: 36px; 
        height: 36px;
        border-radius: 50%;
        border-left-color: #09f;
        animation: spin 1s ease infinite;
    }
    @keyframes spin {
        0%{
            transform: rotate(0deg);
        }
        100%{
            transform: rotate(360deg);
        }
    }
    input{
       
        box-shadow: 0 0 8px rgba(0 0 0 / .3);
        border-radius: .2rem;
    }
::placeholder {
	font-family: 'Amazon Ember', sans-serif;
}
</style>
