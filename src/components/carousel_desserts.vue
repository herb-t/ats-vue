<template>
  <ats_carousel title="Desserts" v-bind:slides="desserts" id="desserts"></ats_carousel>
</template>

<script>
import carousel from './carousel.vue'

export default {
  name: 'carousel_desserts',
  data () {
    return {
      desserts: [
        {
          url: 'http://placekitten.com/250/250'
        },
        {
          url: 'http://placekitten.com/300/300'
        },
        {
          url: 'http://placekitten.com/350/350'
        },
        {
          url: 'http://placekitten.com/400/400'
        },
        {
          url: 'http://placekitten.com/450/450'
        },
        {
          url: 'http://placekitten.com/500/500'
        },
        {
          url: 'http://placekitten.com/550/550'
        },
        {
          url: 'http://placekitten.com/600/600'
        },
        {
          url: 'http://placekitten.com/250/250'
        },
        {
          url: 'http://placekitten.com/300/300'
        },
        {
          url: 'http://placekitten.com/350/350'
        },
        {
          url: 'http://placekitten.com/400/400'
        },
        {
          url: 'http://placekitten.com/450/450'
        },
        {
          url: 'http://placekitten.com/500/500'
        },
        {
          url: 'http://placekitten.com/550/550'
        },
        {
          url: 'http://placekitten.com/600/600'
        },
      ],
    }
  },
  components: {
    ats_carousel: carousel,
	}
}
</script>
