<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <!-- v-show checks expressions are true like an if statement, if true displays or hides the element with display none -->
    <div v-show="1 === 0">
      This is not true, but is hidden by display none
    </div>
  </section>
</template>
<script>
export default {
  name: 'VShow',
  data () {
    return {
      title: 'v-show',
      awesome: true
    }
  }
}
</script>
<style scoped lang="scss">

</style>
