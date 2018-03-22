<template>
  <div>
    <h2>События</h2>
    <p>введите сообщение и нажмите Enter</p>
    <input type="text" v-model="message" v-on:keyup.enter="visible = true"> <br>
    <button v-on:click.prevent="onClick" v-if="visible">Button</button>
  </div>
</template>

<script>
export default {
  name: 'method',
  data () {
    return {
      visible: false,
      message: ''
    }
  },
  methods: {
    onClick: function () {
      alert(this.message)
    }
  }
}
</script>
<style lang="sass">
  button
    margin-top: 10px
    cursor: pointer
    text-transform: uppercase
    font-size: 18px
    background: transparent
    padding: 10px
    border-radius: 3px
    box-shadow: 0 2px 5px 2px rgba(0, 0, 0, 0.2)
    &:hover
      background-color: rgba(0, 0, 0, 0.2)

</style>
