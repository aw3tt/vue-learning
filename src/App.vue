<script>
export default {
  data() {
    return {
      obj: { x: 1, y: 2, z: 3 },
    }
  },
  methods: {
    show: function() {
      alert(Date());
    }
  }
}
</script>

<template>
  <button @mouseover="show">text</button>
</template>
