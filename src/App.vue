<script>
export default {
  data() {
    return {
    obj: {
          user1: '100$',
          user2: '200$',
          user3: '300$',
    }
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
    <li v-for="(el) in obj">{{el}}</li>
  </ul>
  <ul>
    <li v-for="(el, key) in obj">{{key}} - {{el}}</li>
  </ul>
  <ul>
    <li v-for="(el, key, index) in obj">{{key}} - {{el}} - {{index}}</li>
  </ul>
  <ul>
    <li v-for="(el, key, index) in obj">{{key}} - {{el}} - {{index + 1}}</li>
  </ul>
</template>
