<script>
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
  .delete-button {
    background-color: rgba(255, 255, 255, 0);
    border: none;
    margin-left: auto;
    margin-bottom: 0;
  }
  .delete-button::after {
    content: "x";
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
        <button class="delete-button" on:click={() => deleteTodo(todo.id)} />
      </li>
    {/each}
  </ul>
</div>
