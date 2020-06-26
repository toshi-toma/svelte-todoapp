<script>
  export let selectFilter;
  export let updateFilter;
  const handleAllFilterSelect = () => updateFilter("all");
  const handleActiveFilterSelect = () => updateFilter("active");
</script>

<style>

</style>

<ul>
  <li>
    <button on:click={handleAllFilterSelect}>All</button>
  </li>
  <li>
    <button on:click={handleActiveFilterSelect}>Active</button>
  </li>
</ul>
