<template>
  <section class="section section__not-working">
    <h2 class="section__title">{{title}}</h2>
    <div class="form">
      <select v-model="allTurtles">
        <option disabled>Select a turtle</option>
        <option :key="turtle.key" v-for="turtle in allTurtles" :value="turtle.value">
          {{turtle.id}}
        </option>
      </select>
    </div>
  </section>
</template>
<script>
export default {
  name: 'FormSelect',
  data () {
    return {
      title: 'Select',
      allTurtles: [
        {
          id: 'Donatello'
        },
        {
          id: 'Michelangelo'
        },
        {
          id: 'Rafael'
        },
        {
          id: 'Leonardo'
        }
      ]
    }
  }
}
</script>
