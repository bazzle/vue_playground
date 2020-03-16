<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <p v-html="link"></p>
  </section>
</template>
<script>
export default {
  name: 'VHtml',
  data () {
    return {
      title: 'v-HTML',
      link: '<a href="https://www.bbc.co.uk/">BBC</a>'
    }
  },
  methods: {
    doSomething () {
      alert('clicked')
    }
  }
}
</script>
