<style>

  .flickity-viewport {
    padding-bottom: 24px;
  }

  .flickity-button-icon {
    fill: #cf6059 !important;
  }

  .flickity-page-dots {
    height: 32px;
  }

  .flickity-page-dots .dot {
    background: #cf6059 !important;
  }

  .overview__mobile .flickity-viewport {
    overflow: initial;
  }

  .overview__mobile .flickity-page-dots .dot {
    background: #fff !important;
  }

  @media (max-width: 601px) {
    .flickity-button {
      display: none;
    }
  }

  .carousel-cell {
    align-items: center;
    counter-increment: carousel-cell;
    display: flex;
    height: 270px;
    justify-content: center;
    margin-right: 14px;
    width: 270px;
  }

  .carousel-cell img {
    border-radius: 4px;
    box-shadow: 0 3px 6px rgba(0,0,0,.16), 0 3px 6px rgba(0,0,0,.23);
    height: auto;
    margin: 10px;
    max-width: 250px;
    width: 100%;
  }

  .carousel__title {
    margin-top: 0;
    text-transform: uppercase;
  }

  .carousel__copy {
    background: url(/static/images/title-bg-cakes.png) no-repeat center center;
    background-size: 900px;
    text-align: center;
  }

  .carousel__divider {
    background-color: #cf6059;
    box-shadow: 0 3px 6px rgba(0,0,0,.16), 0 3px 6px rgba(0,0,0,.23);
    margin: 54px 0;
    padding: 14px 0;
    width: 100%;
  }

  .carousel__divider svg {
    display: block;
    fill: #fff;
    height: 24px;
    margin: 0 auto;
    width: 24px;
  }

  .carousel:nth-of-type(3) .carousel__divider {
    display: none;
  }

  @media (max-width: 901px) {
    .flickity-page-dots {
      box-sizing: border-box !important;
      padding: 0 16px !important;
    }
  }

  @media (min-width: 900px) {
    .carousel__copy {
      background: url(/static/images/title-bg-cupcakes.png) no-repeat center center;
      background-size: 1080px;
    }
  }

</style>

<template>
  <div class="carousel">
    <div class="carousel__copy">
      <h1 class="carousel__title">{{ title }}</h1>
    </div>

    <flickity :id="id" ref="flickity" :options="flickityOptions">
      <div class="carousel-cell" v-for="slide in slides" :key="slide.id">
        <img :src="slide.url">
      </div>
    </flickity>

    <div class="carousel__divider">
      <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="42.443px" height="42.444px" viewBox="0 0 42.443 42.444" enable-background="new 0 0 42.443 42.444" xml:space="preserve">
      <path class="icon-asterisk-fill" d="M39.782,18.697H28.924c-0.631,0-0.884-0.758-0.505-1.137l7.702-7.702c0.884-0.884,1.137-2.525,0.252-3.535
        c-1.01-1.137-2.651-1.263-3.661-0.126l-7.828,7.828c-0.379,0.379-1.137,0.126-1.137-0.505V2.661c0-1.389-1.01-2.524-2.272-2.651
        c-1.516-0.126-2.778,1.011-2.778,2.525v10.985c0,0.631-0.757,0.884-1.136,0.505L9.731,6.197C8.722,5.187,6.954,5.187,6.07,6.323
        c-0.884,1.01-0.632,2.525,0.252,3.535l7.702,7.702c0.379,0.379,0.127,1.137-0.505,1.137H2.661c-1.389,0-2.525,1.01-2.651,2.272
        c-0.126,1.515,1.01,2.777,2.525,2.777H13.52c0.632,0,0.884,0.758,0.505,1.137l-7.701,7.702c-1.011,1.01-1.137,2.777,0,3.788
        c0.505,0.378,1.136,0.631,1.641,0.631c0.632,0,1.263-0.253,1.769-0.758l7.828-7.828c0.379-0.379,1.136-0.126,1.136,0.505v10.859
        c0,1.389,1.011,2.524,2.273,2.651c1.515,0.126,2.777-1.011,2.777-2.525V28.924c0-0.631,0.758-0.884,1.137-0.505l7.828,7.828
        c0.505,0.505,1.137,0.758,1.768,0.758c0.632,0,1.263-0.253,1.642-0.631c1.01-1.011,1.01-2.778,0-3.788l-7.702-7.702
        c-0.632-0.632-0.379-1.137,0.505-1.137h10.985c1.515,0,2.651-1.263,2.524-2.777C42.308,19.707,41.045,18.697,39.782,18.697z"></path>
      </svg>
    </div>

    <!-- if you don't want to use the buttons Flickity provides -->
    <!-- <button @click="previous()">Custom Previous Button</button>
    <button @click="next()">Custom Next Button</button> -->
  </div>
</template>

<script>
import Flickity from 'vue-flickity'

export default {
  name: 'carousel',
  props: ['title', 'slides', 'id'],
  data () {
    return {
      label: 'carousel',
      flickityOptions: {
        initialIndex: 0,
        prevNextButtons: true,
        pageDots: true,
        wrapAround: true,
        imagesLoaded: true
        // any options from Flickity can be used
      }
    }
  },
  components: {
    Flickity
  },
  methods: {
    next() {
      this.$refs.flickity.next()
    },
    
    previous() {
      this.$refs.flickity.previous()
    }
  }
}
</script>
