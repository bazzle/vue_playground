
<!-- 3 parts to every vue component – template, script, data -->

<!-- this is the component template -->
<template>
  <div id="app">
    <ReceiveData msg = "Hi" name = "Barry" :userNum = 48573 />
    <ThisKeyword />
    <Conditionals />
    <VShow />
    <VIf />
    <VIf2 amihandsome = 'indeed' />
    <VBindConditional />
    <VForArray />
    <VHtml />
    <VFor />
    <VModel />
    <VModel2 />
    <FormSelect />
    <Event />
    <vOn />
    <AccessEventObject />
    <eventModifiers />
    <eventKeyModifiers />
    <FilterSimple />
    <FilterAdvanced />
    <LifecycleEvents />
    <ComputedProperties />
  </div>
</template>

<script>
// import JS files
import ThisKeyword from './components/thiskeyword'
import ReceiveData from './components/receiveData'
import Conditionals from './components/conditionals'
import VShow from './components/vShow'
import VIf from './components/vIf'
import VIf2 from './components/vIf2'
import VBindConditional from './components/vBind-conditional'
import VModel2 from './components/vModel2'
import VFor from './components/vFor'
import VForArray from './components/vForArray'
import VModel from './components/vModel'
import FormSelect from './components/formSelect'
import Event from './components/event'
import eventModifiers from './components/eventModifiers'
import eventKeyModifiers from './components/eventKeyModifiers'
import AccessEventObject from './components/AccessEventObject'
import FilterSimple from './components/filterSimple'
import FilterAdvanced from './components/filterAdvanced'
import LifecycleEvents from './components/lifecycleEvents'
import VHtml from './components/VHtml'
import VOn from './components/VOn'
import ComputedProperties from './components/ComputedProperties'
// Export from this file into main.js
export default {
  // every component needs a name
  name: 'app',
  // define components imported into this component, these names need to match imports
  components: {
    ThisKeyword,
    ReceiveData,
    Conditionals,
    VShow,
    VHtml,
    VIf,
    VIf2,
    VOn,
    VBindConditional,
    VModel2,
    VFor,
    VForArray,
    VModel,
    FormSelect,
    Event,
    eventKeyModifiers,
    AccessEventObject,
    FilterSimple,
    FilterAdvanced,
    LifecycleEvents,
    eventModifiers,
    ComputedProperties
  }
}
</script>

<!-- this is global styling -->
<style lang="scss">
@import "~@/assets/styles/_variables.scss";
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  a{
    color:white;
  }
  body {
    background-color: black;
    width: 100%;
    font-family: 'Fira Code', monospace;
    font-weight:100;
    font-size:16px;
    line-height: 1.4;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  h1, h2, h3, h4, h5, p, ul{
    padding-bottom:0;
    margin-bottom:1em;
  }
  ul, li{
    list-style-type: none;
  }
  button{
    background-color:transparent;
    border:white 1px solid;
    padding:1em 1.4em;
    color:white;
    display:inline-block;
    font-family: inherit;
    font-size:inherit;
    cursor:pointer;
    margin-bottom:1rem;
  }
  select{
    display:inline-block;
    font-size:1.2em;
    padding:2em;
    background-color:rgba(255,255,255,.1);
    color:white;
  }
  input{
    background-color:transparent;
    border:1px solid white;
    padding:1em;
    color:white;
    font-size:1em;
    font-family:inherit;
    margin-bottom:1em;
  }
  .label-input{
    display:flex;
    flex-direction:column;
    justify-content: center;
    align-items:center;
    span{
      display:block;
      padding-bottom:1em;
    }
  }
  #app {
    width: 100%;
    max-width: 800px;
    border: white 1px solid;
    border-radius:6px;
    color:white;
    text-align: center;
    padding:$gap;
    margin: $gap;
  }
    .box{
    padding:1em;
    margin:.5em 0;
    background-color:rgba(255,255,255,.1);
    border-radius: 10px;
  }
  .section{
    border-bottom:1px solid white;
    padding:$gap 0;
    position:relative;
    &__title{
      margin-bottom:$gap/2;
    }
    &__not-working{
      &:after{
        position:absolute;
        right:0;
        top:0;
        padding-top:$gap/2;
        display:block;
        font-size:1.4em;
        content:'Not working 🤮';
        color:red;
      }
    }
    &__needs-work{
      &:after{
        position:absolute;
        right:0;
        top:0;
        padding-top:$gap/2;
        display:block;
        font-size:1.4em;
        content:'Needs work 😓';
        color:red;
      }
    }
    &:first-of-type{
      padding-top:0;
    }
    &:last-of-type{
      border-bottom:0;
      padding-bottom:0;
    }
  }
</style>
