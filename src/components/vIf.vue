<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <!-- checks if a data key exists called handsome/awesome -->
    <p>Are you awesome or handsome or both?</p>
    <p v-if="handsome && awesome">
      Yes, I'm handsome and awesome
    </p>
    <p v-else-if="handsome">
      Yes, I'm handsome
    </p>
    <p v-else-if="awesome">
      Yes, I'm handsome
    </p>
    <p v-else>
      Unfortunately, I'm neither handsome nor awesome 😥
    </p>

  </section>
</template>
<script>
export default {
  name: 'VIf',
  data () {
    return {
      awesome: true,
      handsome: false,
      count: 1,
      title: 'V-if'
    }
  }
}
</script>
<style scoped lang="scss">
  @import "~@/assets/styles/_variables.scss";
</style>
