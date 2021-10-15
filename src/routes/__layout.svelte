<script>
    //import tailwind css
    import "../global.css"
    import "../styles/tailwind-output.css";
    //import header component from lib folder
    import  Header from '$lib/header.svelte';
    import  Footer from '$lib/footer.svelte'; 

</script>

  <!-- Try some classes here -->

  <Header/>
  <main>
      <!-- this is where the content from the route is inserted -->
      <slot></slot>
  </main>

  <h1 class="uppercase text-indigo-500">
    Hello World
  </h1>


  <h1 class="uppercase text-pink-500">
    Referenses
  </h1>

  <Footer/> 