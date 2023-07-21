<!--
  Things to learn:
  + Bindings
  + State (reactivity)
  + ## Comment in Svelte
-->

<script>
	let todo = '';
	export let todos;
	$: console.log({ todos });

	function handleAddTodo(e) {
		e.preventDefault();
		// TODO: side effect ex
		const newTodo = { name: todo, status: 'todo' };
		todos = [...todos, newTodo];
		todo = '';
	}
</script>

<form action="" on:submit={handleAddTodo}>
	<input type="text" bind:value={todo} placeholder="What need to be done?" />
</form>
