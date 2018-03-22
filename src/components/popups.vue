<template>
  <div>
    <h2>Popups</h2>
    <a href="#" @click.prevent="visible = !visible">link</a>
    <div class="popup" v-show="visible">
      <div class="popup__inner">
        <div class="popup__text">
          <slot></slot>
        </div>
        <div class="popup__btns">
          <a href="#" @click.prevent="visible = !visible">close</a>
          <a href="#" @click.prevent="visible = !visible">close</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'popup',
  data () {
    return {
      visible: false
    }
  }
}
</script>
<style lang="sass">
  .popup
    position: fixed
    top: 0
    left: 0
    height: 100%
    width: 100%
    background-color: rgba(0, 0, 0, 0.8)
    &__inner
      position: absolute
      top: 50%
      left: 50%
      transform: translate(-50%, -50%)
      background-color: #FFF
      border-radius: 5px
    &__text
      padding: 50px
      min-width: 500px
      text-align: center
    &__btns
      display: flex
      border-top: 1px solid deepskyblue
      a
        padding: 10px 20px
        width: 50%
        &:first-child
          border-right: 1px solid deepskyblue

</style>
