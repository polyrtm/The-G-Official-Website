<style>
 .flex-container {
     display: flex;
     flex-wrap: wrap;
     justify-content: space-evenly;
     align-content: space-around;
 }

 .soundcloud {
     flex-basis: 400px;
 }

 iframe {
     width: 100%;
 }

 @media only screen and (max-width: 500px) {
     .soundcloud {
	 flex-grow: 1;
	 flex-basis: auto;
	 padding: 1rem 0;
     }
 }
</style>
<script>
 const songs = [
     {
	 title: "Initiation",
	 src: "https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/749475481&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"
     },
     {
	 title: "EB2",
	 src: "https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/749475802&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"
     },
     {
	 title: "Sunset",
	 src: "https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/749476138&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"
     }
 ]
</script>
<h1>
    Our Music
</h1>
<p>Here you will find recordings of our songs, along with scores.</p>
<h2>Demos</h2>
<p>Demos of our songs.</p>

<div class="flex-container">
    {#each songs as song}
	<div class="soundcloud">
	    <iframe title="Initiation" height="300" scrolling="no" frameborder="no" allow="autoplay" {...song}></iframe>
	</div>
    {/each}
</div>

<h2>Scores</h2>
<p>Coming Soon</p>

