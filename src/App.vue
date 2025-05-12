<script>
export default {
  data() {
    return {
      isAuth: true
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <button @click="isAuth = !isAuth">Скрыть</button>
  <template v-if="isAuth">
    <p>+++</p>
    <p>+++</p>
    <p>+++</p>
  </template>

</template>
