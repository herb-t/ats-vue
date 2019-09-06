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
    let _body = document.querySelector('body')
    let _modal = this.$el.querySelector('.modal');
    let _modalContainer = _modal.querySelector('.modal__container');
    let _modalBackdrop = _modal.querySelector('.modal__backdrop');
    let elements = this.$el.querySelectorAll('.modal-toggle');

    const tl = new TimelineMax({paused: true});

    tl.to(_modal, 0.1, {
      autoAlpha: 1,
    });
    tl.to(_modalBackdrop, 0.2, {
      autoAlpha: 1,
      ease: Linear.easeOut
    })
    tl.to(_modalContainer, 0.3, {
      autoAlpha: 1,
      y: '-50%',
      x: '-50%',
      ease: Power4.easeOut
    }, 0.025);

    for (let index = 0; index < elements.length; index++) {
      const element = elements[index];

      element.addEventListener('click', () => {
        if (!_modal.classList.contains('modal-is-showing')) {
          _body.classList.add('modal-is-showing')
          _modal.classList.add('modal-is-showing')
          tl.play();
        } else {
          _body.classList.remove('modal-is-showing')
          _modal.classList.remove('modal-is-showing')
          tl.reverse();
        }
      });
    }
  },
}
</script>
