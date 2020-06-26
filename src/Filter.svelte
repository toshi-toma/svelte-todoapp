<script>
  export let selectFilter;
  export let updateFilter;
  const handleAllFilterSelect = () => updateFilter("all");
  const handleActiveFilterSelect = () => updateFilter("active");
  const handleCompletedFilterSelect = () => updateFilter("completed");
</script>

<style>
  .filter-list {
    display: flex;
    justify-content: center;
    list-style-type: none;
  }
  .filter-item {
    margin-right: 16px;
  }
  .filter-button {
    background-color: #fff;
    border: none;
    cursor: pointer;
  }
  .active-filter {
    border-bottom: 1px solid #ccc;
  }
</style>

<ul class="filter-list">
  <li class="filter-item">
    <button
      class="filter-button"
      class:active-filter={selectFilter === 'all'}
      on:click={handleAllFilterSelect}>
      All
    </button>
  </li>
  <li class="filter-item">
    <button
      class="filter-button"
      class:active-filter={selectFilter === 'active'}
      on:click={handleActiveFilterSelect}>
      Active
    </button>
  </li>
  <li class="filter-item">
    <button
      class="filter-button"
      class:active-filter={selectFilter === 'completed'}
      on:click={handleCompletedFilterSelect}>
      Completed
    </button>
  </li>
</ul>
