<script>
export default {
  data() {
    return {
      isAdmin: true
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
    <p v-if="isAdmin">+++</p>
    <p v-else>---</p>
  </div>

</template>
