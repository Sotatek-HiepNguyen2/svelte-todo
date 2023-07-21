<!--
  Using:
  + prop
  + binding event handler
-->

<script>
	export let idx;
	export let todos;

	function deleteTodo() {
		delete todos[idx];
		todos = todos;
	}
</script>

<li class="todo">
	<input type="checkbox" />
	<div>{todos[idx].name}</div>
	<button on:click={deleteTodo}>x</button>
</li>

<style>
	.todo {
		display: flex;
		gap: 1rem;
	}
</style>
