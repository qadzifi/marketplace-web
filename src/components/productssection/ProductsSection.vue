<script setup lang="ts"></script>

<script lang="ts">
import SearchLensIcon from './assets/images/magnifying-glass-solid.svg';
import FilterIcon from './assets/images/filter-solid.svg';

export default {
  data() {
    return {
      searchLensIcon: SearchLensIcon,
      filterIcon: FilterIcon,
    };
  },
};
</script>

<template>
  <div id="products-container">
    <div id="products-header">
      <h3>
        or browse our full <br />
        Collection
      </h3>
    </div>
    <div id="product-search-bar">
      <div id="product-input-search">
        <img class="search-input-icon" :src="searchLensIcon" />
        <input type="search" placeholder="search" name="search-input" />
      </div>
      <div id="product-input-filter">
        <img class="search-input-icon" :src="filterIcon" />
        <select name="filter-input" id="input-filter-select">
          <option value="">Filter</option>
          <option value="1">Option 1</option>
          <option value="2">Option 2</option>
        </select>
      </div>
    </div>
  </div>
</template>

<style>
:root {
  --size-search-icon: 20px;
  --size-search-field: 22vw;
}

div#products-container {
  margin-top: 40px;
  width: 90vw;
}

div#products-header {
  text-align: center;
}

div#products-header * {
  color: var(--color-brand-yellow);
  font-weight: bold;
}

div#product-search-bar {
  display: flex;
  justify-content: space-between;
}

div#product-input-search,
div#product-input-filter {
  background-color: #ddd;
  padding: 5px;
  display: flex;
  align-content: center;
  border-radius: 4px;
}

div#product-input-search {
  width: var(--size-search-field);
}

img.search-input-icon {
  width: var(--size-search-icon);
  height: var(--size-search-icon);
}

div#product-input-search input {
  margin-left: 5px;
  border: none;
  outline: none;
  color: unset;
  background: none;
}

::placeholder {
  color: blue;
}

div#product-input-search input * {
  color: blue;
}

select#input-filter-select {
  margin-left: 5px;
  width: 10vw;
  border: none;
  outline: none;
  background: none;
}
</style>
