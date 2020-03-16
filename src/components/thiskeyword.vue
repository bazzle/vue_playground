<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <p>Print component to console using 'this'</p>
    <button v-on:click="doSomething">Click here</button>
    <p>Print any data attribute to the console to console using 'this'</p>
    <button v-on:click="printAttribue(title)">This title</button>
    <button v-on:click="printAttribue(someNum)">This number</button>
    <button v-on:click="printAttribue(someArray)">This array</button>
  </section>
</template>
<script>
export default {
  name: 'ThisKeyword',
  data () {
    return {
      title: 'This keyword',
      someNum: 34342,
      someArray: ['red', 'blue', 'green']
    }
  },
  methods: {
    doSomething () {
      console.log(this)
    },
    printAttribue (i) {
      console.log(i)
    }
  }
}
</script>
