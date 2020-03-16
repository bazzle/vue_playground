<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <button v-on:click="age--">-1</button>
    <button v-on:click="age++">+1</button>
    <br><br>
    <button
    v-on:click="plusMinus('minus',5)"
    v-on:dblclick="plusMinus('minus',10)">
      Minus five
    </button>
    <button
    v-on:click="plusMinus('plus',5)"
    v-on:dblclick="plusMinus('plus',10)">
      Plus five
    </button>
    <p>{{age}}</p>
  </section>
</template>
<script>
export default {
  name: 'VOn',
  data () {
    return {
      title: 'v-on',
      age: 35
    }
  },
  methods: {
    plusMinus: function (plusOrMinus, num) {
      if (plusOrMinus === 'plus') {
        this.age = this.age + num
      } else if (plusOrMinus === 'minus' && this.age > 9) {
        this.age = this.age - num
      }
    }
  }
}
</script>
