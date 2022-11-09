<script lang="ts">
import NewsImage from './assets/images/pexels-rodnae-productions-8500340.jpg';

export default {
  data: function () {
    return {
      newsImage: NewsImage,
    };
  },
  computed: {
    newsTop() {
      return {
        'background-image': `url(${this.newsImage})`,
        'background-size': 'cover',
      };
    },
  },
};
</script>

<template>
  <div id="news-and-promos">
    <div id="news-image-container">
      <div id="news-top">
        <img :src="newsImage" />
        <div id="news-text">
          <h1>Text</h1>
        </div>
      </div>
    </div>
    <div id="news-carousel">
      <img :src="newsImage" />
      <img :src="newsImage" />
      <img :src="newsImage" />
      <img :src="newsImage" />
      <img :src="newsImage" />
    </div>
    <div id="promos-section">
      <div id="promos-title">
        <h6>Check out<br />our newest</h6>
      </div>
    </div>
  </div>
</template>

<style>
div#news-and-promos * {
  color: black;
}

div#news-image-container {
  display: flex;
  justify-content: center;
}

div#news-image-container div#news-top {
  height: 300px;
  width: 90vw;
}

div#news-top img {
  height: 300px;
  width: 100%;
  object-fit: cover;
  position: absolute;
  z-index: -1;
}

div#news-top {
  display: flex;
  border-left: 2px solid grey;
  border-right: 2px solid grey;
  background: linear-gradient(
    76deg,
    white,
    white,
    white,
    transparent,
    transparent,
    transparent,
    transparent
  );
}

div#news-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  color: blue;
  margin-left: 40px;
}

div#news-text * {
  font-weight: bold;
}

div#news-carousel {
  margin-top: -10px;
  width: 100%;
  display: flex;
  flex-wrap: nowrap;
  overflow-x: hidden;
}

div#news-carousel img {
  width: 25vw;
  height: 15vw;
  object-fit: cover;
  margin-right: 20px;
  flex: 0 0 auto;
}
</style>
