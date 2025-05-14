<script>
export default {
  data() {
    return {
      arr: ['b', 'c', 'a'],
    }
  },
  methods: {
    add: function() {
      const dateNow = new Date();
      this.arr.push(dateNow);
    },
    remove_first_value: function() {
      this.arr.splice(0, 1)
    },
    remove_last_value: function() {
      this.arr.pop()
    },
    remove_prelast_value: function() {
      this.arr.splice(-2, 1)
    },
    sort_desc: function() {
      this.arr.sort()
    },
    sort_asc: function() {
      this.arr.sort((a, b) => b.localeCompare(a))
    }

  },
  computed: {

  }
}
</script>

<template>
<!--  №1-->
  <ul v-for="item in arr">
    <li>{{item}}</li>
  </ul>
  <button @click="add">add</button>
  <!--  №2-->
  <button @click="remove_first_value">remove first</button>
  <!--  №3-->
  <button @click="remove_last_value">remove last</button>
  <!--  №4-->
  <button @click="remove_prelast_value">remove prelast</button>
  <!--  №5-->
  <button @click="sort_desc">sort_desc</button>
  <!--  №6-->
  <button @click="sort_asc">sort_asc</button>
</template>
