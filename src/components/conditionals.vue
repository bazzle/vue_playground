<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <p v-if="1 === 1">
      Yes, one is one
    </p>
  </section>
</template>
<script>
export default {
  name: 'Conditionals',
  data () {
    return {
      title: 'Basic conditionals'
    }
  }
}
</script>
<style scoped lang="scss">
  @import "~@/assets/styles/_variables.scss";
</style>
