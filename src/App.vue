<script>
export default {
  data() {
    return {
      visible: {
        1: true,
        2: true,
        3: true
      }
    }
  },
  methods: {
    toggle: function(num) {
      this.visible[num] = !this.visible[num]
    },
  },
  computed: {

  }
}
</script>

<template>
  <div>
    <button @click="toggle(1)">{{ visible[1] ? 'Показать 1' : 'Скрыть 1' }}</button>
    <button @click="toggle(2)">{{ visible[2] ? 'Показать 2' : 'Скрыть 2' }}</button>
    <button @click="toggle(3)">{{ visible[3] ? 'Показать 3' : 'Скрыть 3' }}</button>

    <p v-if="visible[1]">Абзац 1</p>
    <p v-if="visible[2]">Абзац 2</p>
    <p v-if="visible[3]">Абзац 3</p>
  </div>

</template>
