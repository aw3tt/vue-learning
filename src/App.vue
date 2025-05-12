<script>
export default {
  data() {
    return {
      visible: true
    }
  },
  methods: {
    hide: function() {
      this.visible = false
    },
    show: function() {
      this.visible = true
    }
  },
  computed: {

  }
}
</script>

<template>
  <button @click="hide">hide</button>
  <button @click="show">show</button>
  <p v-if="visible">text</p>
</template>
