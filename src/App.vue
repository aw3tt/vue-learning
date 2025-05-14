<script>
export default {
  data() {
    return {
      obj: {
        hidden: true,
      },
    }
  },
  methods: {
    show: function () {
      this.obj.hidden = false
    },
    hide: function () {
      this.obj.hidden = true
    },
    toggle: function () {
      this.obj.hidden = !this.obj.hidden
    }
  },
  computed: {

  }
}
</script>

<template>
  <p :class="obj">Some text</p>
  <button @click="show">Show text</button>
  <button @click="hide">Hide text</button>
  <button @click="toggle">Toggle text</button>
</template>

<style>
  p.hidden {
    display: none;
  }
</style>