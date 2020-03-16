<template>
  <section class="section" ref="container">
    <h2 class="section__title">{{title}}</h2>
    <button v-on:click.once="yellowIt" class="yellowIt">
      Click here to make everything all {{ this.allYellow ? 'Black again' : 'Yellow' }}
    </button>
    <br><br>
    <p class="notice" v-show="this.allYellow">You can't make it black again using the button above, because it has the .once event modifier. You need to refresh the page</p>
    <br><br>
    <a v-on:click.prevent="popup" href="https://www.theguardian.com/uk">The Guardian</a>
  </section>
</template>
<script>
export default {
  name: 'eventModifiers',
  data () {
    return {
      title: 'Event Modifiers',
      allYellow: false
    }
  },
  methods: {
    yellowIt: function () {
      if (this.allYellow === true) {
        this.$refs['container'].classList.remove('yellow')
        this.allYellow = false
      } else {
        this.$refs['container'].classList.add('yellow')
        this.allYellow = true
      }
    },
    popup: function () {
      alert('Link clicked, the browser is prevented from its normal action of loading that page')
    }
  }
}
</script>
<style lang="scss" scoped>
  section{
    &.yellow{
      background-color:yellow;
      &>*{
        color:black;
      }
      button{
        border:2px solid black;
      }
    }
    .notice{
      max-width:400px;
      margin: 0 auto;
    }
  }
</style>
