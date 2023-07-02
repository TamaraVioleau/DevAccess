<script>
    import Router from "svelte-spa-router";

  import HomePage from "./views/HomePage.svelte";

  import NavBar from "./components/NavBar.svelte";
  import Footer from "./components/Footer.svelte";

  const routes ={
    "/": HomePage,
  }

</script>

<NavBar/>
<HomePage/>
<Footer/>