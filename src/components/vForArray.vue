<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <div class="form">
      <label class="label-input">
        <span>Add new item</span>
        <!-- this adds a new game to the newgame array -->
        <input type="text" v-model="newGame" v-on:keyup.enter="addNewGame"/>
      </label>
      <!-- can also do event like @click, or @keyup -->
      <button class="button" v-on:click="addNewGame">Add new game</button>
    </div>
    <ul class="games box">
      <li class="games__item" :key="item" v-for="item in myGames">
        {{item}}
      </li>
    </ul>
  </section>
</template>
<script>
export default {
  name: 'VForArray',
  data () {
    return {
      title: 'v-for Array loop',
      newGame: '',
      myGames: ['days Gone', 'Fifa 18']
    }
  },
  methods: {
    addNewGame: function () {
      this.myGames.push(this.newGame)
      this.newGame = ''
    }
  }
}
</script>
<style lang="scss" scoped>
  @import "~@/assets/styles/_variables.scss";
  .button{
    margin-bottom:2em;
  }
</style>
