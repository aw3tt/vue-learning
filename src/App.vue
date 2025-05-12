<script>
export default {
  data() {
    return {
      age: 20
    }
  },
  methods: {
    getAgeCategory() {
      if (this.age < 18) return 'подросток';
      if (this.age <= 25) return 'молодой человек';
      return 'мужчина';
    }
  },
  computed: {

  }
}
</script>

<template>
  <div>
    <p v-if="age < 18">подросток</p>
    <p v-else-if="age <= 25">молодой человек</p>
    <p v-else>мужчина</p>
  </div>

</template>
