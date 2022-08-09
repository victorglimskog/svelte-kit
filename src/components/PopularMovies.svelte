<script>
    import MovieCard from "./MovieCard.svelte";
    export let popular;
</script>

<div class="flex justify-center">
    <div class="flex-col text-center">
        <h1 class="text-2xl my-2">Popular Movies</h1>
        <div class="flex flex-wrap">
            {#each popular as movie}
                <MovieCard {movie} />
            {/each}
        </div>
    </div>
</div>
