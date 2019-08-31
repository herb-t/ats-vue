<style scoped>
  .gallery {
    
  }
</style>

<template>
  <div class="gallery">
    <!-- <div class="ats-main">
      <div class="gallery__title">
        <h1>{{title}}</h1>
      </div>
    </div> -->

    <ats_carousel_cakes></ats_carousel_cakes>
    <ats_carousel_cupcakes></ats_carousel_cupcakes>
    <ats_carousel_desserts></ats_carousel_desserts>

  </div>
</template>

<script>
import carousel_cakes from './carousel_cakes.vue'
import carousel_cupcakes from './carousel_cupcakes.vue'
import carousel_desserts from './carousel_desserts.vue'

export default {
  name: 'gallery',
  data () {
    return {
      title: 'Gallery'
    }
  },
  components: {
    ats_carousel_cakes: carousel_cakes,
    ats_carousel_cupcakes: carousel_cupcakes,
    ats_carousel_desserts: carousel_desserts
	}
}
</script>
