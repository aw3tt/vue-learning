<script>
export default {
  data() {
    return {
      arr: [],
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <div style="display:flex">
    <input type="checkbox" v-model="arr" value="Анлийский">
    <p>Анлийский</p>
  </div>
  <div style="display:flex">
    <input type="checkbox" v-model="arr" value="Французский">
    <p>Французский</p>
  </div>
  <div style="display:flex">
    <input type="checkbox" v-model="arr" value="Немецкий">
    <p>Немецкий</p>
  </div>
  <ul>
    <li v-for="item in arr">{{item}}</li>
  </ul>
</template>

<style>

</style>