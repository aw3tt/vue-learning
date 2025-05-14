<script>
export default {
  data() {
    return {
      newItem: '',
      items: ['a', 'b', 'c', 'd', 'e'],
    }
  },
  methods: {
    addItem() {
      if (this.newItem.trim()) {
        this.items.unshift(this.newItem.trim());
        this.newItem = '';
      }
    },
    removeItem(index) {
      this.items.splice(index, 1);
    }
  }
}
</script>

<template>
  <div>
    <ul>
      <li
          v-for="(item, index) in items"
          :key="index"
          @click="removeItem(index)"
      >
        {{ item }}
      </li>
    </ul>
    <input v-model="newItem" @keyup.enter="addItem">
    <button @click="addItem">Добавить</button>
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>