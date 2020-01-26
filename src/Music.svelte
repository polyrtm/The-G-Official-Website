<style>
 .flex-container {
     display: flex;
     flex-wrap: wrap;
     justify-content: space-evenly;
     align-content: space-around;
 }

 .item {
     flex-basis: 400px;
 }

 .item > * {
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
	 src: "https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/749475481&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true",
	 score: "assets/Initiation.pdf",
	 thumbnail: "/assets/Initiation.png"
     },
     {
	 title: "EB2",
	 src: "https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/749475802&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true",
	 score: "assets/EB2.pdf",
	 thumbnail: "/assets/EB2.png"
     },
     {
	 title: "Sunset",
	 src: "https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/749476138&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true",
	 score: "assets/sunset.pdf",
	 thumbnail: "/assets/Sunset.png"
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
    {#each songs as {src, title}}
	<div class="item">
	    <iframe height="300" scrolling="no" frameborder="no" allow="autoplay" {src} {title}/>
	</div>
    {/each}
</div>

<h2>Scores</h2>
<div class="flex-container">
    {#each songs as {score, thumbnail, title}}
	<div class="item">
	    <a href={score}><img src={thumbnail} alt={title} {title}></a>
	</div>
    {/each}
</div>


