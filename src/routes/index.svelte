<script contetext="module">
    export const prerender = true
    import Counter from "$lib/counter.svelte";
</script>


<section>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>


<h2>Let's learn Svelte</h2>
<p>lorem ipsum</p>

<Counter></Counter>

</section>
<!-- scoped styling -->
<style>
    section {
        min-height : calc (100vh - var(--header-height));
        display: grid;
        place-items: center;
        place-content: center;
    }
</style>