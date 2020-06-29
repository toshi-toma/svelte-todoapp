<script>
  export let todo;
  export let deleteTodo;
  let isEditing = false;
  const toggleEditing = () => (isEditing = !isEditing);
</script>

<style>
  .todo-item {
    display: flex;
    height: 30px;
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

<li class="todo-item">
  <input
    type="checkbox"
    class="doneCheckbox"
    title="Done"
    bind:checked={todo.isDone} />
  {#if isEditing}
    <form on:submit={toggleEditing}>
      <input type="text" bind:value={todo.content} />
    </form>
  {:else}
    <div on:click={toggleEditing}>{todo.content}</div>
  {/if}
  <button class="delete-button" on:click={() => deleteTodo(todo.id)} />
</li>
