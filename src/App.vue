<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5],
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
    <p v-for="el in items">{{el}}</p>
  </div>
  <p>-------------------</p>
  <div>
    <p v-for="el in items">{{Math.pow(el, 2)}}</p>
  </div>
  <ul>
    <li v-for="el in items">{{el}}</li>
  </ul>
</template>
