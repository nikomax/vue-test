<template>
  <div>
    <h2>Список</h2>
    <ul class="list">
      <li class="list__item" v-bind:key="item" v-for="item in bears" v-bind:class="{ 'strike': item.status}">{{item.name}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'list',
  data () {
    return {
      bears: [
        {
          name: 'гризли',
          status: false
        }, {
          name: 'гризли',
          status: false
        }, {
          name: 'панда',
          status: true
        }, {
          name: 'гризли',
          status: false
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass">

</style>
