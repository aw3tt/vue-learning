<script>
export default {
  data() {
    return {
      message: 'hello',
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <input v-model="message">
  <p>{{ message.toUpperCase() }}</p>

  <input v-model="message">
  <p>{{ Math.pow(message, 2) }}</p>
</template>

<style>

</style>