<script>
export default {
  data() {
    return {
      isClicked: false
    }
  },
  methods: {
    handleClick() {
      if (!this.isClicked) {
        this.isClicked = true;
      }
    }
  },
  computed: {

  }
}
</script>

<template>
  <button @click="handleClick" :disabled="isClicked">
    {{ isClicked ? 'Уже нажато' : 'Нажми меня' }}
  </button>
</template>
