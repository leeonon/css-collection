<script>
	import Card from './Card.svelte';
</script>

<div class="list">
	<Card />
	<Card />
	<Card />
	<Card />
	<Card />
	<Card />
	<Card />
	<Card />
	<Card />
</div>

<style>
	.list {
		width: 800px;
		padding: 30px;
		display: grid;
		gap: 15px;
		background-color: black;
		grid-template-columns: repeat(3, minmax(0, 1fr));
	}
</style>
