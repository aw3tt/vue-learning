<script>
export default {
  data() {
    return {

    }
  },
  methods: {
    handleClick(event) {
      event.preventDefault(); // Блокируем переход
      alert("Запрещено");
    }
  },
  computed: {

  }
}
</script>

<template>
  <a href="https://google.com" @click="handleClick">Google</a>
</template>
