<template>
  <div>
    <h2>Переходы</h2>
    <button @click="visible = !visible">Button</button>
    <div class="box" v-show="visible" transition="slide"></div>
  </div>
</template>

<script>
export default {
  name: 'show',
  data () {
    return {
      visible: false
    }
  }
}
</script>
<style lang="sass">
  .box
    margin: 10px auto
    height: 100px
    width: 100px
    background-color: mistyrose
    border: 1px dotted blue
  .slide-transition
    transition: all 0.3s
  .slide-enter
    left: -100%
  .slide-leave
    left: -100%
</style>
