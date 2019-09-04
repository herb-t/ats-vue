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

export default {
  name: 'index',
  components: {
    ats_header: site_header,
    ats_hero: hero,
    ats_overview: overview,
    ats_gallery: gallery,
    ats_services: services,
    ats_contact: contact,
    ats_modal: modal
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
          tl.play();
          body_.classList.add('modal-is-showing')
        } else {
          modal_.classList.remove('modal-is-showing')
          tl.reverse();
          body_.classList.remove('modal-is-showing')
        }
      });
    }
  },
}
</script>
