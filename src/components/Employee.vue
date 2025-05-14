<script>
export default {
  emits: ['remove'],
  props: ['id', 'name', 'surn'],
  data() {
    return {

    }
  },
  methods: {

  },
}
</script>
<template>
  {{ name }}
  {{ surn }}

  <button @click="$emit('remove', id)">
    remove
  </button>
</template>