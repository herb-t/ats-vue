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
  </main>

</template>

<script>
import site_header from './header.vue'
import hero from './hero.vue'
import overview from './overview.vue'
import gallery from './gallery.vue'
import services from './services.vue'
import contact from './contact.vue'

export default {
  name: 'index',
  components: {
    ats_header: site_header,
    ats_hero: hero,
    ats_overview: overview,
    ats_gallery: gallery,
    ats_services: services,
    ats_contact: contact
	}
}
</script>
