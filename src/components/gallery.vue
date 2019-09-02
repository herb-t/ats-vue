<style scoped>
  .gallery {
    margin: 54px 0;
  }
</style>

<template>
  <div class="gallery" id="gallery">

    <ats_carousel title="Cakes" v-bind:slides="cakes" id="cakes"></ats_carousel>

    <ats_carousel title="Cupcakes" v-bind:slides="cupcakes" id="cupcakes"></ats_carousel>

    <ats_carousel title="Desserts" v-bind:slides="desserts" id="desserts"></ats_carousel>

  </div>
</template>

<script>
import carousel from './carousel.vue'

import {cakes, cupcakes, desserts} from './data/carousel.js'

export default {
  name: 'gallery',
  data () {
    return {
      title: 'Gallery',
      cakes: cakes,
      cupcakes: cupcakes,
      desserts: desserts
    }
  },
  components: {
    ats_carousel: carousel,
	}
}
</script>
