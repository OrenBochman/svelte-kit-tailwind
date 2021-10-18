<script context="module">
    export async function load({ page,fetch }) {
      
        const dev_to_api = `https://dev.to/api/articles/${page.params.slug}`
        const response = await fetch(dev_to_api)
        const post = await response.json()
      return {
        props: {
          post
        }
      }
    }
  </script>

<script>
    export let post
</script>
  
<svelte:head>
    <title>{post.title}</title>
</svelte:head>
  
<article>
    <h1>{post.title}</h1>
    {@html post.body_html}
  </article>
