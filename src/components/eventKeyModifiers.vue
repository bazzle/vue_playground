<template>
  <section class="section">
    <h2 class="section__title">{{title}}</h2>
    <p>Type in your name please, hit return when done</p><br/>
    <input type="text" v-model="nameEntry" v-on:keyup.enter="nameInput" />
    <p>{{name}}</p>
  </section>
</template>
<script>
export default {
  name: 'eventKeyModifiers',
  data () {
    return {
      title: 'Event Key Modifiers',
      nameEntry: '',
      name: ''
    }
  },
  methods: {
    nameInput: function () {
      this.name = this.nameEntry
    }
  }
}
</script>
