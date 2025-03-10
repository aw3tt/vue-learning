<script>
export default {
  data() {
    return {
      obj: { x: 1, y: 2, z: 3 },
    }
  },
}
</script>

<template>
  <p>{{ obj.x + obj.y + obj.z }}</p>
</template>
