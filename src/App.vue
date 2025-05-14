<script>
export default {
  data() {
    const days = ['Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота', 'Воскресенье'];
    const months = ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'];
    const years = [2020, 2021, 2022, 2023, 2024, 2025];

    const currentDate = new Date();
    const currentDayIndex = currentDate.getDay();
    const currentMonthIndex = currentDate.getMonth();
    const currentYear = currentDate.getFullYear();

    const adjustedDayIndex = currentDayIndex === 0 ? 6 : currentDayIndex - 1;

    return {
      selected: 'Не выбран',
      days: days,
      selectedDay: days[adjustedDayIndex],
      months: months,
      selectedMonth: months[currentMonthIndex],
      years: years,
      selectedYear: currentYear
    }
  },
  created() {
    if (!this.years.includes(this.selectedYear)) {
      this.years.push(this.selectedYear);
      this.years.sort();
    }
  }
}
</script>

<template>
  <div>
    <select v-model="selected">
      <option v-for="day in days">{{ day }}</option>
    </select>
    <p>{{ selected }}</p>

    <select v-model="selectedDay">
      <option v-for="day in days">{{ day }}</option>
    </select>
    <select v-model="selectedMonth">
      <option v-for="month in months">{{ month }}</option>
    </select>
    <select v-model="selectedYear">
      <option v-for="year in years">{{ year }}</option>
    </select>

    <p>День недели: {{ selectedDay }}</p>
    <p>Месяц: {{ selectedMonth }}</p>
    <p>Год: {{ selectedYear }}</p>
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>