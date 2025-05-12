<script>
export default {
  data() {
    return {
      visible: true
    }
  },
  methods: {
    toggle: function() {
      this.visible = !this.visible
    },
  },
  computed: {

  }
}
</script>

<template>
  <button @click="toggle">{{ visible ? 'Скрыть' : 'Показать' }}</button>
  <p v-if="visible">text</p>
</template>
