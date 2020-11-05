<script>
	let todos = [];
	let newTodo;
	function addTodo(event) {
		todos = [...todos,newTodo];
		newTodo = "";
	}
</script>

<main>
	TODOLIST

	<input type="text" bind:value={newTodo}>
	<button on:click={addTodo}>Ajouter</button>
	
	{#if todos.length > 0}
	Todos
	<ul>
	{#each todos as todo }
	<li>{todo}</li>
		
	{/each}
		</ul>
	{/if}

</main>

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