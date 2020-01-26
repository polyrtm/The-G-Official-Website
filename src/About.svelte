<script>
 import Card from './Card.svelte'
 const bios = [
     {
	 src: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.9FZZxs6TXZPSNRQyY0d-FAHaFj%26pid%3DApi&f=1",
	 name: "Jack",
	 description: "Bass"
     },
     {
	 src: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.9FZZxs6TXZPSNRQyY0d-FAHaFj%26pid%3DApi&f=1",
	 name: "Ethan",
	 description: "Drums/Trombone"
     },
     {
	 src: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.9FZZxs6TXZPSNRQyY0d-FAHaFj%26pid%3DApi&f=1",
	 name: "Patrick",
	 description: "Drums/Synth"
     }
 ]
</script>
<style>
 .cards {
     display: flex;
     flex-wrap:wrap;
     
 }
</style>
<h1>
    About Us
</h1>
<p>Hi! We are The G, a band based in Atlanta, Georgia. We make modern jazz fusion style pieces to perform and share online. We love making and playing music, and want to share our creations with everyone. Enjoy!</p>
<h3>Members:</h3>
<div class="cards">
    {#each bios as member}
	<Card {...member}/>
    {/each}
</div>
