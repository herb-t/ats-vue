<style scoped>
  .ats-main {

  }
</style>

<template>

  <main class="ats-main">
    <ats_header></ats_header>
    <ats_hero></ats_hero>
    <ats_overview></ats_overview>
    <ats_gallery></ats_gallery>
    <ats_services></ats_services>
    <ats_contact></ats_contact>
    <ats_modal></ats_modal>
    <ats_share></ats_share>
  </main>

</template>

<script>
import site_header from './header.vue'
import hero from './hero.vue'
import overview from './overview.vue'
import gallery from './gallery.vue'
import services from './services.vue'
import contact from './contact.vue'
import modal from './modal.vue'
import share from './share.vue'

export default {
  name: 'index',
  components: {
    ats_header: site_header,
    ats_hero: hero,
    ats_overview: overview,
    ats_gallery: gallery,
    ats_services: services,
    ats_contact: contact,
    ats_modal: modal,
    ats_share: share
	},
  mounted: function() {
    let body_ = document.querySelector('body')
    let modal_ = this.$el.querySelector('.modal');
    let modalContainer_ = modal_.querySelector('.modal__container');
    let modalBackdrop_ = modal_.querySelector('.modal__backdrop');
    let elements = this.$el.querySelectorAll('.modal-toggle');

    const tl = new TimelineMax({paused: true});

    tl.to(modal_, 0.1, {
      autoAlpha: 1,
    });
    tl.to(modalBackdrop_, 0.2, {
      autoAlpha: 1,
      ease: Linear.easeOut
    })
    tl.to(modalContainer_, 0.3, {
      autoAlpha: 1,
      y: '-50%',
      x: '-50%',
      ease: Power4.easeOut
    }, 0.025);

    for (let index = 0; index < elements.length; index++) {
      const element = elements[index];

      element.addEventListener('click', () => {
        if (!modal_.classList.contains('modal-is-showing')) {
          modal_.classList.add('modal-is-showing')
          body_.classList.add('modal-is-showing')
          tl.play();
        } else {
          modal_.classList.remove('modal-is-showing')
          body_.classList.remove('modal-is-showing')
          tl.reverse();
        }
      });
    }

    const controller = new ScrollMagic.Controller();
    const shareIn = new TimelineMax();
    const shareOut = new TimelineMax();
    const overview_ = this.$el.querySelector('.overview');
    const services_ = this.$el.querySelector('.services');
    const share_ = this.$el.querySelector('.share');
    
    shareIn.to(share, 0.6, {x: 0});
    shareOut.to(share, 0.6, {x: 500});


    new ScrollMagic.Scene({
      triggerElement: overview_,
      triggerHook: 0,
    })
    .setTween(TweenMax.to(share_, 0.6, {x: 0, ease: Power4.easeOut}))
    .addTo(controller);

    new ScrollMagic.Scene({
      triggerElement: services_,
      triggerHook: 0,
      offset: 80 // move trigger to center of element
    })
    .setTween(TweenMax.to(share_, 0.8, {x: 200, ease: Power2.easeOut}))
    .addTo(controller);

  },
}
</script>
