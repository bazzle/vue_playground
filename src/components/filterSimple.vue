<template>
  <section class="section">
    <h1 class="section__title">{{title}}</h1>
    <p>{{ "This string has been uppercased by filter" | capitalize }}</p>
  </section>
</template>
<script>
export default {
  name: 'FilterSimple',
  data: function () {
    return {
      title: 'Filters'
    }
  },
  filters: {
    capitalize: function (value) {
      console.log(typeof value)
      if (typeof value === 'string') {
        return value.toUpperCase()
      } else {
        console.log('Must be string')
      }
    }
  }
}
</script>
<style scoped lang="scss">
  @import "~@/assets/styles/_variables.scss";
</style>
