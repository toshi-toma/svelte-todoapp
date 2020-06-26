<script>
  import Header from "./Header.svelte";
  import AddTodoForm from "./ToDo/AddTodoForm.svelte";
  import Filter from "./Filter.svelte";
  import TodoList from "./ToDo/TodoList.svelte";

  let todos = [];
  let filter = "active"; // active | all
  const addTodo = todo => {
    todos = [...todos, { content: todo, isDone: false }];
  };
  const updateFilter = nextFilter => (filter = nextFilter);
  $: filteredTodos = todos.filter(todo => {
    if (filter === "active") {
      return !todo.isDone;
    } else if (filter === "all") {
      return true;
    }
    return true; // fallback
  });
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
  <Filter bind:selectFilter={filter} {updateFilter} />
  <TodoList bind:todos={filteredTodos} />
</main>
