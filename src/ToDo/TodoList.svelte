<script>
  export let todos;
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
  .todo-item {
    display: flex;
    padding-bottom: 6px;
    align-items: center;
    border-bottom: 1px solid #f0f0f0;
    margin-bottom: 16px;
  }
  .doneCheckbox {
    margin-bottom: 0;
    margin-right: 6px;
  }
</style>

<div class="wrapper">
  <ul class="todo-list">
    {#each todos as todo}
      <li class="todo-item">
        <input
          type="checkbox"
          class="doneCheckbox"
          title="Done"
          bind:checked={todo.isDone} />
        <div>{todo.content}</div>
      </li>
    {/each}
  </ul>
</div>
