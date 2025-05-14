<script>
export default {
  data() {
    return {
      isDisabled: true,
    }
  },
  methods: {
    toggleDisabled() {
      this.isDisabled = !this.isDisabled
    }
  }
}
</script>

<template>
  <div>
    <input type="text" :disabled="isDisabled" />
    <button @click="toggleDisabled">btn</button>

      <label>
        <input
            type="checkbox"
            @change="toggleDisabled"
        >
        {{ isDisabled ? 'Заблокировано' : 'Разблокировано' }}
      </label>
      <input
          type="text"
          :disabled="isDisabled"
      >
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>