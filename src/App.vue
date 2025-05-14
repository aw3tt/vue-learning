<script>
export default {
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <p :class="{active: true, valid: false}">Some text</p>
</template>

<style>
  p.active {
    background: yellow;
  }
</style>