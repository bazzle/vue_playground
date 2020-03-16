<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <div v-on:click="clickEvent" v-on:mousemove="updatexy" class="square">
      <div class="data">
        <div>
          <span>
            {{xposition}}
          </span>
          <span>
            {{yposition}}
          </span>
        </div>
        <div v-show="clickxposition !== null">
          <span>
            {{clickxposition}}
          </span>
          <span>
            {{clickyposition}}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'AccessEventObject',
  data () {
    return {
      title: 'Access Event Object',
      xposition: 0,
      yposition: 0,
      clickxposition: null,
      clickyposition: null
    }
  },
  methods: {
    updatexy: function (event) {
      this.xposition = event.offsetX
      this.yposition = event.offsetY
    },
    clickEvent: function (event) {
      this.clickxposition = event.offsetX
      this.clickyposition = event.offsetY
    }
  }
}
</script>
<style lang="scss" scoped>
  .square{
    border: 1px solid white;
    width:100%;
    height:300px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
