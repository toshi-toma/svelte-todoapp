<script>
  import Header from "./Header.svelte";
  import AddTodoForm from "./ToDo/AddTodoForm.svelte";
  import TodoList from "./ToDo/TodoList.svelte";

  let todos = [];
  const addTodo = todo => {
    todos = [...todos, { content: todo, isDone: false }];
  };
</script>

<style>
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 16px;
  }
</style>

<Header />
<main>
  <AddTodoForm {addTodo} />
  <TodoList {todos} />
</main>
