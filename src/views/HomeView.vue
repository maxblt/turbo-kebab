<template>
  <div class="home">
    <h1>Testttt</h1>
    <carousel :items-to-show="1">
      <slide v-for="slide in slides" :key="slide">
        <img :src="slide.imageUrl" />
      </slide>

      <template #addons>
        <navigation />
        <pagination />
      </template>
    </carousel>
  </div>
</template>

<script>

import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

export default {
  name: 'HomeView',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data: () => ({
    slides: [
      {
        imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Lula_kebab_2.jpg/800px-Lula_kebab_2.jpg',
        caption: 'Photo by 2'
      },
      {
        imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Lula_kebab_2.jpg/800px-Lula_kebab_2.jpg',
        caption: 'Photo by 2'
      },
      {
        imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Lula_kebab_2.jpg/800px-Lula_kebab_2.jpg',
        caption: 'Photo by 3'
      },
      {
        imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Lula_kebab_2.jpg/800px-Lula_kebab_2.jpg',
        caption: 'Photo by 4'
      }
    ]
  }),
};

</script>

<style>
.home {
  padding: 2%;
}
</style>
