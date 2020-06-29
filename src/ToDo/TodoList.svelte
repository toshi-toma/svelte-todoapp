<script>
  import TodoItem from "./TodoItem.svelte";
  export let todos;
  export let deleteTodo;
</script>

<style>
  .wrapper {
    display: flex;
    justify-content: center;
  }
  .todo-list {
    list-style-type: none;
    width: 300px;
  }
</style>

<div class="wrapper">
  <ul class="todo-list">
    {#each todos as todo}
      <TodoItem {todo} {deleteTodo} />
    {/each}
  </ul>
</div>
