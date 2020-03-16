<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <p>This invokes destruction, will turn component into static that can't be interacted with</p>
    <button v-on:click="toDestroy">Click 🤯</button>
    <div class="checkboxes">
      <label>Donatello
        <input type="checkbox" id="donatello" value="donatello" v-model="checkedTurtles">
      </label>
      <label>Michelangelo
        <input type="checkbox" id="michelangelo" value="michelangelo" v-model="checkedTurtles">
      </label>
      <label>Rafael
        <input type="checkbox" id="rafael" value="rafael" v-model="checkedTurtles">
      </label>
      <label>Leonardo
        <input type="checkbox" id="leonardo" value="leonardo" v-model="checkedTurtles">
      </label>
    </div>
    <div class="turtlegifs">
      <div class="turtlegifs__item" :key="turtle" v-for="turtle in checkedTurtles">
        <img class="turtle"  :src="require(`../assets/turtles/${turtle}.jpg`)"/>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'LifecycleEvents',
  data () {
    return {
      title: 'Component lifecycle events',
      checkedTurtles: [
      ]
    }
  },
  methods: {
    toDestroy: function () {
      this.$destroy()
    }
  },
  created: function () {
    console.log('Lifecycle created')
  },
  mounted: function () {
    console.log('Lifecycle mounted')
  },
  updated: function () {
    console.log('Lifecycle updated')
  },
  destroyed: function () {
    console.log('Lifecycle destroyed')
  }
}
</script>
<style scoped lang="scss">
  .checkboxes{
    margin-bottom:2em;
    display:grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: .5em;
    grid-template-rows: auto;
    label{
      padding:1em;
      background-color:rgba(255,255,255,.1);
      border-radius: 10px;
      line-height:1;
      cursor:pointer;
      &:last-of-type{
        margin-right:0;
      }
    }
  }
  .turtlegifs{
    display:flex;
    align-items:stretch;
    justify-content: center;
    &__item{
      border-radius: 10px;
      background-color:white;
      overflow:hidden;
      display:flex;
      align-items:center;
      margin-right:10px;
      &:last-of-type{
        margin-right:0;
      }
    }
    &__item img{
      object-fit: contain;
      height:auto;
      width:100%;
      max-height:300px;
    }
  }
</style>
