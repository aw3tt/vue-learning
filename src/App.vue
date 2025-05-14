<script>
export default {
  data() {
    return {
      newItem: '',
      items: ['a', 'b', 'c', 'd', 'e'],
    }
  },
  methods: {
    addItem: function() {
      this.items.unshift(this.newItem)
    }
  }
}
</script>

<template>
  <div>
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
      </li>
    </ul>
    <input v-model="newItem">
    <button @click="addItem">add</button>
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>