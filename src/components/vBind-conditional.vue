<template>
  <section class="section">
    <h1 class="section__title">{{title}}</h1>
    <div class="form">
      <label class="label-input">
        <span>Enter email address</span>
        <!-- v-bind can apply class based on outcome of ternary if statement -->
        <input v-bind:class="[emailCheck.length < 4 ? 'red' : 'green']" type="text" v-model="emailCheck">
        <!-- Can also be written like this;
        v-bind:class="{red: email.length < 4}" -->
      </label>
      <p v-if="validation(emailCheck) === false">
        This is not a valid email address
      </p>
      <p v-else>
        Good
      </p>
      <p>If the email does not contain both an @ symbol and a dot, this button won't work</p>
      <!-- with v-bind, or simply : we dynamically change html attribute values -->
      <button
      v-bind:class="[validation(emailCheck) ? 'button--green' : 'button--red']"
      onclick="alert('signed-up')"
      v-bind:disabled="validation(emailCheck) === false">
        Submit
      </button>
    </div>
  </section>
</template>
<script>
export default {
  name: 'VBindConditional',
  data () {
    return {
      title: 'v-bind checking conditions',
      emailCheck: ''
    }
  },
  methods: {
    validation (i) {
      if (i.includes('@') && i.includes('.')) {
        return true
      } else {
        return false
      }
    }
  }
}
</script>
<style lang="scss" scoped>
  @import "~@/assets/styles/_variables.scss";
  $green:rgba(green,.3);
  $red: rgba(red,.3);
  .button{
    &--green{
      background-color:$green;
    }
    &--red{
      background-color:$red;
    }
  }
  .green{
    background-color:$green;
  }
  .red{
    background-color:$red;
  }
</style>
