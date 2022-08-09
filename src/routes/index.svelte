<script context="module">
    export async function load({fetch}){
        const apiKey = 'd377abc08a4fe07e1ce2f502cf0b512c';
        const url = `https://api.themoviedb.org/3/movie/popular?api_key=${apiKey}&language=en-US&page=1`;
        const res = await fetch(url);
        const data = await res.json();
        console.log('data: ', data);
        if(res.ok){
            return {
                props: {popular: data.results}
            };
        }
    }
</script>

<script>
    import PopularMovies from "../components/PopularMovies.svelte";
    export let popular;
</script>

<div class="container mx-auto mt-8">
    <h1 class="text-3xl font-bold text-center">Movie Site</h1>
    <section>
        <PopularMovies {popular} />
    </section>
</div>