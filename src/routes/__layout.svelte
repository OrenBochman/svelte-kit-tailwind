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
      <slot/>
  </main>


  <Footer/> 