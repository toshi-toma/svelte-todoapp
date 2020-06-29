<script>
  import Input from "./Input.svelte";
  let input = "";
  export let addTodo;
  const handeClick = e => {
    e.preventDefault();
    addTodo(input);
    input = "";
  };
</script>

<style>
  form {
    display: flex;
    justify-content: center;
  }
</style>

<form on:submit={handeClick}>
  <Input bind:value={input} />
  <button>Add</button>
</form>
