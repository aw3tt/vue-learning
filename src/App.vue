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
  <p v-show="isAuth">+++</p>
</template>
