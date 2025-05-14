<script>
export default {
  data() {
    return {
      arr: ['x', 'y', 'z'],
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <ul>
    <li v-for="(el, key) in arr">{{key}}</li>
  </ul>
</template>
