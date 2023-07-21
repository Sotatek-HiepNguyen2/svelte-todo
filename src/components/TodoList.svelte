<!--
  Learning:
  + Render list
  + props
-->

<script>
	import TodoItem from './TodoItem.svelte';

	export let todos;
</script>

<ul>
	{#each todos as _, idx}
		<TodoItem {todos} {idx} />
	{/each}
</ul>
