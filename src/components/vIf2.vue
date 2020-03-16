<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <!-- checks if a data key exists called handsome/awesome -->
    <p>Are you awesome or handsome or both?</p>
    <p v-if='amihandsome == "indeed"'>
      Yes, I'm handsome
    </p>

  </section>
</template>
<script>
export default {
  name: 'VIf2',
  data: function () {
    return {
      title: 'v-if 2'
    }
  },
  props: [ 'amihandsome' ]
}
</script>
<style scoped lang="scss">
  @import "~@/assets/styles/_variables.scss";
</style>
