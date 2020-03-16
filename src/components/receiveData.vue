<template>
  <section class="section">
    <h1 class="section__title">{{title}}</h1>
    <p>{{ msg }}, {{ name }},</p>
    <p class="usernum">Unique user number: {{ userNum }}</p>
  </section>
</template>

<script>
export default {
  name: 'ReceiveData',
  data () {
    return {
      title: 'Receive Data'
    }
  },
  // these are props. which are effectively properties/parameters that data gets passed into
  props: {
    msg: String,
    name: String,
    userNum: Number
  },
  watch: {
    messageChange () {
      console.log('messagechanged')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import "~@/assets/styles/_variables.scss";
  .intro{
    margin-bottom:4em;
    padding-bottom:4em;
    border-bottom:1px solid white;
  }
</style>
