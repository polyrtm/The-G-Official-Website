<style>
	span {
		background-color: #800000;
		flex-grow: 1;
		color: white;
		text-align: center;
		line-height: 3rem;
		cursor: pointer;
		font-size: 1.5rem;
	}
	span:hover {
		background-color: #640000
	}
</style>
<script>
	export let text;
	export let setPage;
</script>
<span on:click={
			setPage(text.toLowerCase())
			}>
	{text}
</span>