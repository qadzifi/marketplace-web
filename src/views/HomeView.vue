<script setup lang="ts">
import NewsSection from '@/components/newssection/NewsSection.vue';
import CategoriesSection from '@/components/categoriessection/CategoriesSection.vue';
import ProductsSection from '@/components/productssection/ProductsSection.vue';
</script>

<script lang="ts">
import CartIcon from '@/components/icons/IconCart.svg';

export default {
  data() {
    return {
      cartIcon: CartIcon,
    };
  },
};
</script>

<template>
  <div id="contents-container">
    <div id="button-cart">
      <img :src="cartIcon" />
    </div>
    <NewsSection />
    <CategoriesSection />
    <ProductsSection />
  </div>
</template>

<style>
:root {
  --cart-button-size: 8vmin;
  --cart-button-pos: 5vmin;
  --color-brand-yellow: #ffcf24;
}

div#contents-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

div#button-cart {
  position: fixed;
  z-index: 2;
  right: var(--cart-button-pos);
  bottom: var(--cart-button-pos);
  background-color: var(--color-brand-yellow);
  width: var(--cart-button-size);
  height: var(--cart-button-size);
  display: flex;
  justify-content: center;
  border-radius: 50%;
}

div#button-cart img {
  width: 4vmin;
  filter: invert();
}
</style>
