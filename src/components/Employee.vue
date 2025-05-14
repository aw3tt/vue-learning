<script>
export default {
  emits: ['show', 'show2'],
  props: {
    id: Number,
    name: String,
    salary: Number,
    age: Number,
    key: Number,
  },
  data() {
    return {
      count: 0
    }
  },
  methods: {
    handle() {
      this.$emit('show');
    },
    handle2() {
      this.$emit('show2');
    }
  },
}
</script>
<template>
  <button @click="handle">btn</button>
  <button @click="handle2">btn2</button>
</template>