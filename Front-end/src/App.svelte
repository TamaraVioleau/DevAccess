<script>
    import Router from "svelte-spa-router";

  import HomePage from "./views/HomePage.svelte";

  import NavBar from "./components/NavBar.svelte";

  const routes ={
    "/": HomePage,
  }

</script>

<NavBar/>
<HomePage/>