<template>
  <div id="app">
    <img src="./assets/logo.png">
    <test></test>
    <list></list>
    <method></method>
    <show></show>
    <popup>Text 1</popup>
    <popup>Text 2</popup>
  </div>
</template>

<script>
import test from './components/test'
import list from './components/list'
import method from './components/button'
import show from './components/show'
import popup from './components/popups'
export default {
  name: 'App',
  components: { test, list, method, show, popup }
}
</script>

<style lang="sass">
#app
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  margin-top: 60px

button
  cursor: pointer
  text-transform: uppercase
  font-size: 18px
  background: transparent
  padding: 10px
  border-radius: 3px
  box-shadow: 0 2px 5px 2px rgba(0, 0, 0, 0.2)
  &:hover
    background-color: rgba(0, 0, 0, 0.2)

.list
  list-style: none
  &__item
    margin-bottom: 10px
    &.strike
      text-decoration: line-through
</style>
