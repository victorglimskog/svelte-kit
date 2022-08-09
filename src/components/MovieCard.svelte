<script>
    export let movie;
</script>

<div class="w-1/4 px-2 py-2">
    <a href={`/movie/${movie.id}`}>
        <img class="rounded-md" src={'https://image.tmdb.org/t/p/w500' + movie.poster_path} alt={movie.title}  />
        <h2>{movie.title}</h2>
        <p>{movie.release_date}</p>
    </a>
</div>