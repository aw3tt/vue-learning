<script>
export default {
  data() {
    return {
      selected: 'Город не выбран',
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
    <h3>Выберите город в котором проживаете</h3>
    <select v-model="selected">
      <option>Москва</option>
      <option>Санки-Петербург</option>
      <option>Симферополь</option>
    </select>

    <p>{{ selected }}</p>
  </div>
</template>

<style>

</style>