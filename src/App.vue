<script>
export default {
  data() {
    return {
      isValid: true,
      isDisabled: false,
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <p :class="{active: isDisabled, valid: isValid}">Some text</p>
</template>

<style>
  p.active {
    background: green;
  }
  p.valid {
    background: red;
  }
</style>