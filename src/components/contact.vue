<style scoped>
  .contact {
    margin-bottom: 3000px;
  }
</style>

<template>
  <div class="contact">
    <h1 class="contact__title">{{ label }}</h1>
  </div>
</template>

<script>
export default {
  name: 'contact',
  data () {
    return {
      label: 'Contact'
    }
  }
}
</script>
