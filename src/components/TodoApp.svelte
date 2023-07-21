<script>
	import AddTodo from './AddTodo.svelte';
	import TodoList from './TodoList.svelte';

	let todos = [];
</script>

<AddTodo bind:todos />
<TodoList {todos} />
