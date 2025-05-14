<script>
export default {
  data() {
    return {
      checked: false,
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <div>
    <label>
      <input type="checkbox" v-model="checked">
      Показать абзац
    </label>
    <p v-if="checked">
      Этот абзац виден только когда чекбокс отмечен!
    </p>
  </div>
</template>

<style>

</style>