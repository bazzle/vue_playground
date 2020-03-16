<template>
  <section class="section greeting">
    <h2 class="section__title">{{title}}</h2>
    <!-- v-model directive  -->
    <div class="form">
      <!-- this is the v-model, where the v-model is declared through the input -->
      <input type="text" v-model="greeting">
    </div>
    <!-- v-if checks expressions are true like an if statement, if false, ejects element from the dom -->
    <!-- interesting how this v-if evaluates to false even though greeting is delared in data -->
    <p v-if="greeting">
      Greeting exists
    </p>
    <p>{{greeting}}</p>
    <!-- this text won't update when the v-model input changes -->
    <p v-once>{{greeting}}</p>
  </section>
</template>
<script>
export default {
  name: 'VModel2',
  data () {
    return {
      greeting: 'Helloooo',
      title: 'Using v-model to change text dynamically'
    }
  }
}
</script>
