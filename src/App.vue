<script>
export default {
  data() {
    return {
      day: 1
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
    <p v-if="day === 0">Воскресенье</p>
    <p v-if="day === 1">Понедельник</p>
    <p v-if="day === 2">Вторник</p>
    <p v-if="day === 3">Среда</p>
    <p v-if="day === 4">Четверг</p>
    <p v-if="day === 5">Пятница</p>
    <p v-if="day === 6">Суббота</p>
  </div>

</template>
