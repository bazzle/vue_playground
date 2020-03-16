<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <div class="games">
      <!-- v-bind:key should be a unqiue identifier like this, or game.key or whatever -->
      <div class="games__item box" :key="game.blah" v-for="game in myGames">
        <h2 class="games__item__title">{{game.title}}</h2>
        <ul>
          <li>{{game.platform}}</li>
          <li>{{game.type}}</li>
        </ul>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'VFor',
  data () {
    return {
      title: 'v-for loop',
      newGame: '',
      myGames: [
        {
          id: 'daysgone',
          title: 'Days Gone',
          platform: 'ps4',
          type: 'Zombie shooter'
        },
        {
          id: 'fifa18',
          title: 'Fifa 18',
          platform: 'ps4',
          type: 'Sports sim'
        }
      ]
    }
  }
}
</script>
<style scoped lang="scss">
  @import "~@/assets/styles/_variables.scss";
  .button{
    margin-bottom:4em;
  }
  .games{
    &__item{
      display:flex;
      flex-direction:column;
      &__title{
        font-size:1.4em;
        text-decoration: underline;
      }
    }
  }
</style>
