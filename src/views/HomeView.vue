<template>
  <div class="home">
    <h1>Welcome !</h1>
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
        imageUrl: 'https://bilder.t-online.de/b/87/28/28/82/id_87282882/tid_da/doener-kebab-diese-berliner-spezialitaet-ist-auf-der-ganzen-welt-beruehmt-symbolbild-.jpg',
        caption: 'Our delicious kebab'
      },
      {
        imageUrl: 'https://media.gettyimages.com/photos/kebab-picture-id182199049?s=612x612',
        caption: 'Tasty close-up'
      },
      {
        imageUrl: 'https://media.istockphoto.com/photos/professional-female-cook-with-grilled-meat-on-spit-for-kebab-picture-id628803418',
        caption: 'Our chef'
      },
      {
        imageUrl: 'https://www.canstockphoto.com/zoom/?height=367&width=598&id=86549467&_ts=1647575047714&scale=1.3377926421404682&left=40&top=8',
        caption: 'Incredible service'
      }
    ]
  }),
};

</script>

<style>
.home {
  margin: auto;
  padding: 2%;
  align-items: center;
  text-align: center;
}

section img {
  border : 10px white solid;
  height: 400px;
}
</style>
