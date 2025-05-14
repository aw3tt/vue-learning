<script>
export default {
  data() {
    return {
      items: [1, 2, 3],
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <template v-for="elem in items">
    <div>
      <p>{{elem}}</p>
      <p class ="divider"></p>
    </div>
  </template>
  <ul>
    <tempalate v-for="elem in items">
      <li>{{elem}}</li>
      <li class ="divider"></li>
    </tempalate>
  </ul>
</template>
