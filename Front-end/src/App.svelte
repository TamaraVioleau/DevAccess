<script>
    import Router from "svelte-spa-router";

  import HomePage from "./views/HomePage.svelte";

  import NavBar from "./components/NavBar.svelte";
  import Footer from "./components/Footer.svelte";
  import BlogArticle from "./components/BlogArticle.svelte";

  const routes ={
    "/": HomePage,
  }

</script>

<NavBar/> 
 <!-- <BlogArticle/> -->
<HomePage/> 
<Footer/>