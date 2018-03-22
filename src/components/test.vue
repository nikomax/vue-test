<template>
  <div class="test">
    <h1 v-if="msg">{{msg}}</h1>
    <input type="text" v-model="msg">
  </div>
</template>

<script>
export default {
  name: 'test',
  data () {
    return {
      msg: 'Lol'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass">
  h1
    font-size: 40px
    color: gray
  input
    padding: 5px
    font-size: 22px
    border-radius: 3px
    border: none
    box-shadow: 0px 2px 3px gray

</style>
