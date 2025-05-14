<script>
export default {
  emits: ['func'],
  props: ['name', 'salary'],
  data() {
    return {

    }
  },
  methods: {
    handle() {
      this.$emit('func', this.name, this.salary);
    },
  },
}
</script>
<template>
  <button @click="handle">btn</button>
</template>