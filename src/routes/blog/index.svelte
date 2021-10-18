<script context="module">
    export async function load({ fetch }) {

        const dev_to_api = 'https://dev.to/api/articles?username=brittneypostma'
        const sanity_api = 'https://t295jcoh.api.sanity.io/v1/data/query/production?query=*%5B_type%20in%20%5B%22post%22%2C%20%5D%5D%5B0...2%5D%20%2F%2F%20_type%20is%20movie%20or%20person%0A'
        //const response = await fetch(dev_to_api)
        const response = await fetch(dev_to_api)

        //      const posts = await response.json(sanity_api)
        const posts = await response.json()
      return {
        props: {
          posts,
        },
      }
    }
  </script>
  
  <script>
    export let posts
  </script>
  
  <svelte:head>
    <title>Blog</title>
  </svelte:head>
  
  <section>
    <h1>Blog</h1>
    <ul>
      {#each posts as post}
        <li>
          <a href={`/blog/${post.id}`}> {post.title}</a>
        </li>
      {/each}
    </ul>
  </section>
