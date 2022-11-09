<script setup lang="ts">
import ToolBoxImage from './assets/images/pexels-artem-podrez-8985454.jpg';
</script>

<script lang="ts">
export default {
  data() {
    return {
      toolBoxImage: ToolBoxImage,
    };
  },
};
</script>

<template>
  <div id="categories-container">
    <div id="categories-header">
      <h3>
        Look through our<br />
        Categories
      </h3>
    </div>
    <div id="categories-listing">
      <div>
        <img :src="toolBoxImage" />
        <div class="categories-name">
          <div>Categories Name</div>
        </div>
      </div>
      <div>
        <img :src="toolBoxImage" />
        <div class="categories-name">
          <div>Categories Name</div>
        </div>
      </div>
      <div>
        <img :src="toolBoxImage" />
        <div class="categories-name">
          <div>Categories Name</div>
        </div>
      </div>
      <div>
        <img :src="toolBoxImage" />
        <div class="categories-name">
          <div>Categories Name</div>
        </div>
      </div>
      <div>
        <img :src="toolBoxImage" />
        <div class="categories-name">
          <div>Categories Name</div>
        </div>
      </div>
      <div>
        <img :src="toolBoxImage" />
        <div class="categories-name">
          <div>Categories Name</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
div#categories-container {
  margin-top: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

div#categories-header * {
  text-align: center;
  font-weight: bold;
}

div#categories-listing {
  margin-top: 40px;
  width: 90vw;
  min-height: 13vw;
  display: flex;
  overflow-x: hidden;
}

div#categories-listing > div {
  background: linear-gradient(
    80deg,
    rgba(255, 255, 255, 90%) 5%,
    transparent 35%,
    transparent 60%
  );
}

div#categories-listing > div:not(:last-child) div.categories-name {
  margin-right: 6vw;
}

div#categories-listing div img {
  min-width: 26vw;
  max-height: 13vw;
  object-fit: cover;
  border-radius: 10px;
  z-index: -1;
  position: absolute;
}

div#categories-listing div.categories-name {
  min-width: 26vw;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: end;
}

div.categories-name div {
  max-width: 35%;
  margin-left: 10px;
  margin-bottom: 10px;
  font-weight: bold;
  text-shadow: 2px 2px white;
}
</style>
