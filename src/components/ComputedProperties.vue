<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <button v-on:click="addtoA">Add to A</button>
    <button v-on:click="addtoB">Add to B</button>
    <br><br>
    <span>{{ a }}</span><br>
    <span>{{ b }}</span><br>
    <span>Age + a = {{ age }}</span><br>
  </section>
</template>
<script>
export default {
  name: 'ComputedProperties',
  data () {
    return {
      title: 'Computed Properties',
      age: 36,
      a: 0,
      b: 0
    }
  },
  methods: {
    addtoA: function () {
      this.a++
      this.age = this.age + this.aOlives77
      
    },
    addtoB: function () {
      this.b++
      this.age = this.age + this.a
    }
  }
}
</script>
