<script setup lang="ts">
import { RouterView } from 'vue-router';
import NavigationBar from './components/navbar/NavigationBar.vue';
</script>

<template>
  <NavigationBar />

  <div id="content-container">
    <RouterView />
  </div>
</template>

<style scoped></style>
