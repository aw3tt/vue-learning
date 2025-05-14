<script>
export default {
  data() {
    return {
      cssClasses: 'btn',
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <button :class="cssClasses">Button</button>
</template>

<style>
  .btn:hover {
    background: orange;
  }
</style>