<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <button v-on:click="doSomething">Click here</button>
  </section>
</template>
<script>
export default {
  name: 'Event',
  data () {
    return {
      title: 'Basic event'
    }
  },
  methods: {
    doSomething () {
      alert('clicked')
    }
  }
}
</script>
