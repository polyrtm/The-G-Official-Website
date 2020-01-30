<link href="https://fonts.googleapis.com/css?family=Exo:800|Teko&display=swap" rel="stylesheet">
<style>
    .container {
    width: 100%;
    height: auto;
    color: white;
    padding: 1rem;
    box-sizing: border-box;
    }
    .content {
    margin: 1em;
    padding: 1rem;
    background-color: #383d3f;
    }
    .content h1 {
    font-family: 'Exo';
    }
    :global(body) {
    padding: 0;
    background-color: rgb(45, 49, 51);
 }
</style>
<script>
 import NavBar from './NavBar.svelte'
 import Home from './Home.svelte'
 import About from './About.svelte'
 import Music from './Music.svelte'
 import Contact from './Contact.svelte'
 let name = 'world';
 let page = "home";
</script>
<svelte:window/>
<NavBar setPage="{newPage => {
		 page = newPage;
		 window.scroll({
		     top: 0,
		     left: 0,
		     behavior: 'smooth'
		 });
		 }}"/>
<div class="container">
<div class="content">
{#if page == "home"}
    <Home/>
{:else if page == "about us"}
    <About/>
{:else if page == "our music"}
    <Music/>
{:else if page == "contact"}
    <Contact/>

{:else}
	404: Not Found
{/if}

</div>
</div>
<svelte:head>
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- The G Website Bottom -->
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-4378637561054189"
     data-ad-slot="2213998906"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
</svelte:head>