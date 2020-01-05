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
	let name = 'world';
	let page = "home";
	let y;
</script>
<svelte:window bind:scrollY={y}/>
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
    <div style="text-align:center">
	<h1>
		The G
	</h1>
	<h2>Music Coming Soon</h2>
	</div>
{:else if page == "about us"}
	<h1>
		About Us
	</h1>
	<p>Hi! We are The G, a band based in Atlanta, Georgia. We make modern jazz fusion style pieces to perform and share online. We love making and playing music, and want to share our creations with everyone. Enjoy!</p>
<h3>Members:</h3>

<p>Jack - Bass</p>
<p>Ethan -Drumset/Trombone</p>
<p>Patrick - Drumset/???</p>
{:else if page == "our music"}
	<h1>
		Our Music
	</h1>
	<p>Here you will find recordings of our songs, along with scores.</p>
	<h1>Soon</h1>
{:else if page == "contact"}
	<h1>
		Contact Us
	</h1>
	<p>Contact us by email, or via twitter.</p>
	<h3>Main Email:</h3>
	<a href="mailto:contact@the-g.org">contact@the-g.org</a>
	<h3>Member Emails:</h3>
	<a href="mailto:ethan@the-g.org">ethan@the-g.org</a>
	<br>
	<a href="mailto:jack@the-g.org">jack@the-g.org</a>
	<br>
	<a href="mailto:patrick@the-g.org">patrick@the-g.org</a>
	<h3>Twitter</h3>
	<a href="https://twitter.com/TheG_Music">@TheG_Music</a>

{:else}
	404: Not Found
{/if}

</div>
</div>
