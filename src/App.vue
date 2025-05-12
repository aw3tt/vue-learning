<script>
export default {
  data() {
    return {
      num1: 1,
      num2: 2,
    }
  },
  methods: {
    show: function() {
      alert(this.getDayName(3));
    },
    getDayName: function (dayNumber) {
      const days = ['Воскресенье', 'Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота'];
      if (dayNumber < 0 || dayNumber > 6) {
        return 'Неверное число! Допустимо: 0-6';
      }
      return days[dayNumber];
    },
  }
}
</script>

<template>
  {{show()}}
</template>
