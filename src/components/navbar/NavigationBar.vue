<script setup lang="ts">
import BrandIcon from '../icons/IconBrand.vue';
</script>

<template>
  <div class="navbar-container">
    <div id="navbar-left">
      <BrandIcon />
    </div>
    <div id="navbar-middle">
      <nav>
        <RouterLink to="/#news">News</RouterLink>
        <RouterLink to="/#promos">Promos</RouterLink>
        <RouterLink to="/#categories">Categories</RouterLink>
        <RouterLink to="/#browse">Browse</RouterLink>
      </nav>
    </div>
    <div id="navbar-right">
      <nav>
        <RouterLink to="/login">Login</RouterLink>
      </nav>
    </div>
  </div>
</template>

<style>
div.navbar-container {
  position: sticky;
  top: 0;
  height: 60px;
  display: flex;
  justify-content: space-between;
  background-color: white;
  z-index: 1;
  margin-bottom: 20px;
  box-shadow: 0px 2px 4px lightgrey;
}

div.navbar-container nav {
  display: flex;
  width: min-content;
  margin: 0;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--ps-color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

div#navbar-left,
div#navbar-right {
  width: 240px;
}

div#navbar-right {
  display: flex;
  justify-content: flex-end;
}

@media (min-width: 1024px) {
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
