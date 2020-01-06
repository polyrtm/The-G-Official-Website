<script>
 export let name;
 export let src;
 export let description;
</script>
<style>
 .card {
     flex-grow: 1;
     background-color: rgb(45, 49, 51);
     color: white;
     padding: 1rem;
     margin: 1rem;
     transition: .25s ease all;
     border: 4px #640000 solid;
 }
 .card:hover {
     border: 4px #d00000 solid;
 }
 img {
     width: 100%;
 }
</style>
<div class="card">
    <img {src} alt={name}>
    <h3>
	{name}
    </h3>
    <p>
	{description}
    </p>
</div>
