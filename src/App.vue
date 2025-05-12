<script>
export default {
  data() {
    return {
      visible: false
    }
  },
  methods: {
    hide: function() {
      this.visible = true
    }
  },
  computed: {

  }
}
</script>

<template>
  <button @click="hide">hide</button>
  <p v-if="visible">text</p>
</template>
