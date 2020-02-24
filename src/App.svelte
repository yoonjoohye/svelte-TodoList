<script>
	let txt='';
	let todos=[];

	const save=()=>{
		todos=todos.concat(txt);
	}
</script>


	<input type="text" bind:value={txt}/>
	<button on:click={save}>추가</button>

	{#each todos as todo}
		<div>{todo}</div>
	{/each}


<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>