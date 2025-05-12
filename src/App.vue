<script>
export default {
  data() {
    return {
      visible: true
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
  <button @click="() => visible = !visible">Поменять</button>
  <p v-if="visible">visible = true</p>
  <p v-if="!visible">visible = false</p>
</template>
