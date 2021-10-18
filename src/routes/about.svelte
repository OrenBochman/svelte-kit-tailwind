<script context="module">

    import {browser,dev} from "$app/env"
    export const hydrare = dev
    export const router = browser
    export const prerender = true
</script>

<svelte:head><title>About</title></svelte:head>

<section>
    <h1>About SvelteKit</h1>
    <p>This is the about page</p>
</section>