<style>
  /*! Flickity v2.2.1
  https://flickity.metafizzy.co
  ---------------------------------------------- */
  .flickity-enabled {
    position: relative;
  }

  .flickity-enabled:focus { outline: none; }

  .flickity-viewport {
    overflow: hidden;
    position: relative;
    height: 100%;
  }

  .flickity-slider {
    position: absolute;
    width: 100%;
    height: 100%;
  }

  /* draggable */

  .flickity-enabled.is-draggable {
    -webkit-tap-highlight-color: transparent;
    -webkit-user-select: none;
      -moz-user-select: none;
        -ms-user-select: none;
            user-select: none;
  }

  .flickity-enabled.is-draggable .flickity-viewport {
    cursor: move;
    cursor: -webkit-grab;
    cursor: grab;
  }

  .flickity-enabled.is-draggable .flickity-viewport.is-pointer-down {
    cursor: -webkit-grabbing;
    cursor: grabbing;
  }

  /* ---- flickity-button ---- */

  .flickity-button {
    position: absolute;
    background: hsla(0, 0%, 100%, 0.75);
    border: none;
    color: #333;
  }

  .flickity-button:hover {
    background: white;
    cursor: pointer;
  }

  .flickity-button:focus {
    outline: none;
    box-shadow: 0 0 0 5px #19F;
  }

  .flickity-button:active {
    opacity: 0.6;
  }

  .flickity-button:disabled {
    opacity: 0.3;
    cursor: auto;
    /* prevent disabled button from capturing pointer up event. #716 */
    pointer-events: none;
  }

  .flickity-button-icon {
    fill: currentColor;
  }

  /* ---- previous/next buttons ---- */

  .flickity-prev-next-button {
    top: 50%;
    width: 44px;
    height: 44px;
    border-radius: 50%;
    /* vertically center */
    transform: translateY(-50%);
  }

  .flickity-prev-next-button.previous { left: 10px; }
  .flickity-prev-next-button.next { right: 10px; }
  /* right to left */
  .flickity-rtl .flickity-prev-next-button.previous {
    left: auto;
    right: 10px;
  }
  .flickity-rtl .flickity-prev-next-button.next {
    right: auto;
    left: 10px;
  }

  .flickity-prev-next-button .flickity-button-icon {
    position: absolute;
    left: 20%;
    top: 20%;
    width: 60%;
    height: 60%;
  }

  /* ---- page dots ---- */

  .flickity-page-dots {
    position: absolute;
    width: 100%;
    bottom: -25px;
    padding: 0;
    margin: 0;
    list-style: none;
    text-align: center;
    line-height: 1;
  }

  .flickity-rtl .flickity-page-dots { direction: rtl; }

  .flickity-page-dots .dot {
    display: inline-block;
    width: 10px;
    height: 10px;
    margin: 0 8px;
    background: #333;
    border-radius: 50%;
    opacity: 0.25;
    cursor: pointer;
  }

  .flickity-button-icon {
    fill: #cf6059 !important;
  }

  .flickity-page-dots .dot.is-selected {
    opacity: 1;
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

  .carousel__copy {
    text-align: center;
  }

</style>

<template>
  <div class="carousel">
    <div class="carousel__copy">
      <h1 class="carousel__title">{{ title }}</h1>
    </div>

    <flickity :id="id" ref="flickity" :options="flickityOptions">
      <div class="carousel-cell" v-for="slide in slides">
        <img :src="slide.url">
      </div>
    </flickity>

    <!-- if you don't want to use the buttons Flickity provides -->
    <!-- <button @click="previous()">Custom Previous Button</button>
    <button @click="next()">Custom Next Button</button> -->
  </div>
</template>

<script>
import Flickity from 'vue-flickity';

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
      },
    }
  },
  components: {
    Flickity
  },
  methods: {
    next() {
      this.$refs.flickity.next();
    },
    
    previous() {
      this.$refs.flickity.previous();
    }
  }
}
</script>
