<style scoped>
  .services {

  }
</style>

<template>
  <div class="services">
    <h1 class="services__title">{{ label }}</h1>
  </div>
</template>

<script>
export default {
  name: 'services',
  data () {
    return {
      label: 'Services'
    }
  }
}
</script>
