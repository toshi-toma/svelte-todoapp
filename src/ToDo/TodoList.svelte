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
    border-bottom: 1px solid #f0f0f0;
    margin-bottom: 16px;
  }
</style>

<div class="wrapper">
  <ul class="todo-list">
    {#each todos as todo}
      <li class="todo-item">
        <div>{todo}</div>
      </li>
    {/each}
  </ul>
</div>
