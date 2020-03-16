<template>
  <section class="section">
    <h1 class="section__title">{{title}}</h1>
    <p>{{ "I am having a good day" | whatEmoji(emoji) | capitalize }}</p>
  </section>
</template>
<script>
export default {
  name: 'FilterAdvanced',
  data: function () {
    return {
      title: 'Filters advanced usage',
      emoji: '🙂'
    }
  },
  filters: {
    // Filters pass the object it is filtering through to the function via value parameter
    whatEmoji: function (value, emoji) {
      if (typeof value === 'string') {
        return `${emoji} ${value}`
      } else {
        console.log('Must be string')
      }
    },
    capitalize: function (value) {
      return value.toUpperCase()
    }
  }
}
</script>
<style scoped lang="scss">
  @import "~@/assets/styles/_variables.scss";
</style>
