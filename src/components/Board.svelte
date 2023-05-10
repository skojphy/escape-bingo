<script>
	import Square from './Square.svelte';
	import bingo from '../data/new.json';
	import Title from './Title.svelte';
</script>

<div class="board">
	<div class="title">
		<Title {bingo} />
	</div>
	<ul>
		{#each bingo.itemList as item}
			<Square isChecked={false} themeName={item.name} />
		{/each}
	</ul>
</div>

<style>
	.board {
		max-width: 600px;
		width: 90%;
		min-width: 300px;
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
	}
	.title {
		width: 100%;
		margin-bottom: 15px;
		font-size: 18px;
	}
	ul {
		display: grid;
		grid-template-columns: repeat(5, 1fr);
		grid-template-rows: repeat(5, 1fr);
		width: 90vw;
		height: 90vw;
		min-width: 300px;
		min-height: 300px;
		max-width: 600px;
		max-height: 600px;
		border: 1px solid black;
	}
</style>
