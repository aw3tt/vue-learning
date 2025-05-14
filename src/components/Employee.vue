<script>
export default {
  emits: ['func'],
  props: ['name', 'salary'],
  data() {
    return {

    }
  },
  methods: {

  },
}
</script>
<template>
  <button @click="$emit('func', this.name, this.salary);">btn</button>
</template>