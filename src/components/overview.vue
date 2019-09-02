<style scoped>
  .overview {
    background: #cf6059;
    box-shadow: 0 3px 6px rgba(0,0,0,.16), 0 3px 6px rgba(0,0,0,.23);
    padding: 54px 0;
  }

  .overview__card {
    margin-bottom: 54px;
    text-align: center;
  }

  .overview__card:last-of-type {
    margin-bottom: 0;
  }

  .overview__card-container {
    background: #fff;
    border-radius: 4px;
    box-shadow: 0 10px 20px rgba(0,0,0,.19), 0 6px 6px rgba(0,0,0,.23);
    margin: 0 auto;
    max-width: 400px;
    /* opacity: 0; */
    padding: 24px 16px;
    transform: translateY(500px);
  }

  .overview__card-title,
  .overview__card-subtitle,
  .overview__card-text {
    margin-bottom: 24px;
    margin-top: 0;
  }

  .overview__card-title {
    margin-top: 24px;
  }

  .overview__card-subtitle {
    font-size: 16px;
    font-weight: 400;
    margin-bottom: 12px;
  }

  .overview__card-text {
    margin-bottom: 8px;
  }

  .icon-asterisk-fill {
    fill: #cf6059;
  }

  .overview__card-cta {
    margin-top: 54px;
  }

  .overview__card-br {
    background: #cf6059;
    display: block;
    margin: 0 auto 24px;
    height: 1px;
    width: 100px;
  }

  @media (min-width: 900px) {
    .overview {
      padding: 100px 0;
    }
    .overview__card {
      margin: 0 1.03799%;
    }

    .overview__card-container {
      max-width: 100%;
      padding: 42px 16px;
    }
  }
</style>

<template>
  <div class="overview" id="overview">
    <div class="ats-page">
      <div class="ats-grid">
        <div class="overview__card ats-grid__col ats-grid__col--3" v-for="card in cards">
          <div class="overview__card-container" :id="card.id">
            <div class="overview__card-icon">
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

            <h2 class="overview__card-title" v-html="card.title">{{card.title}}</h2>
            <div class="overview__card-br"></div>

            <h4 class="overview__card-subtitle">{{card.subtitle}}</h4>
            <p class="overview__card-text">{{card.serving1}}</p>
            <p class="overview__card-text">{{card.serving2}}</p>
            <p class="overview__card-text">{{card.serving3}}</p>

            <div class="overview__card-cta">
              <button class="ats-button modal-toggle">{{cta_label}}</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'overview',
  data () {
    return {
      label: 'Overview',
      cta_label: 'Find out more',
      cards: [
        {
          id: 'one',
          title: 'Two Layer<br>Sheet Cake',
          subtitle: 'STARTS @ $30',
          serving1: '1/4 Serves 25 - 30 Guests',
          serving2: '1/2 Serves 50 - 60 Guests',
          serving3: 'Full Serves 80 - 90 Guests'
        },
        {
          id: 'two',
          title: 'Three Layer<br>Sheet Cake',
          subtitle: 'STARTS @ $30',
          serving1: '6" Serves 15 - 18 Guests',
          serving2: '8" Serves 30 - 35 Guests',
          serving3: '10" Serves 40 - 45 Guests'
        },
        {
          id: 'three',
          title: 'Two Layer<br>Round Cake',
          subtitle: 'STARTS @ $25',
          serving1: '6" Serves 10 - 12 Guests',
          serving2: '8" Serves 25 - 30 Guests',
          serving3: '10" Serves 35 - 40 Guests'
        }
      ]
    }
  },
  mounted: function() {
    let controller = new ScrollMagic.Controller();

    const tl = new TimelineMax();
    tl.to("#one", 1, {y: 0, autoAlpha: 1, ease: Power2.easeOut});
    tl.to("#two", 1, {y: 0, autoAlpha: 1, ease: Power3.easeOut}, 0.25);
    tl.to("#three", 1, {y: 0, autoAlpha: 1, ease: Power4.easeOut}, 0.5);

    new ScrollMagic.Scene({
      triggerElement: ".overview",
      triggerHook: "onEnter", // show, when scrolled 10% into view
      duration: "80%", // use full viewport
      // offset: 50 // move trigger to center of element
    })
    .setTween(tl)
    .addTo(controller);
  }
}
</script>
