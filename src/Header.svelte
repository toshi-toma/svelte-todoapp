<script>
  import AddTodoForm from "./ToDo/AddTodoForm.svelte";
</script>

<style>
  header {
    display: flex;
    background-color: tomato;
    color: white;
    height: 100px;
  }
  .header-link {
    display: flex;
    justify-content: center;
  }
  .header-img {
    width: 100px;
  }
  .header-title {
    display: flex;
    align-items: center;
    margin-left: 16px;
  }
</style>

<header>
  <a href="https://svelte.dev/" class="header-link">
    <img src="/svelte-logo.svg" alt="" class="header-img" />
  </a>
  <h1 class="header-title">ToDo App</h1>
</header>
