<script>
export default {
  props: ['arg'],
  data() {
    return {

    }
  }
}
</script>
<template>
  <ul>
    <li v-for="ar in arg">{{ar}}</li>
  </ul>
</template>