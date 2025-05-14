<script>
export default {
  data() {
    return {
      first_num: 0,
      second_num: 0,
      num: 0,
      res: 0,
      text1: '',
      text2: '',
      fullName: '',
      lastName: '',
      firstName: '',
      middleName: ''
    }
  },
  methods: {
    calc: function() {
      this.res = Math.pow(this.num, 1/2);
    },
    sum: function() {
      this.res = this.first_num + this.second_num;
    },
    changeText: function() {
      const text1 = this.text1;
      const text2 = this.text2;
      this.text2 = text1
      this.text1 = text2
    },
    splitName: function() {
      const parts = this.fullName.trim().split(' ').filter(part => part !== '');

      this.lastName = parts[0] || '';
      this.firstName = parts[1] || '';
      this.middleName = parts[2] || '';
    }
  },
  computed: {

  }
}
</script>

<template>
  <p>Калькулятор корня</p>
  <input v-model="num">
  <button v-on:click="calc">work</button>
  <p>{{ res }}</p>

  <p>Калькулятор суммы</p>
  <input type="number" v-model="first_num">
  <input type="number" v-model="second_num">
  <button v-on:click="sum">Calculate Sum</button>
  <p>{{ res }}</p>

  <p>Смена текстов инпута</p>
  <input type="text" v-model="text1">
  <input type="text" v-model="text2">
  <button v-on:click="changeText">Change text</button>

  <p>Пользователь</p>
  <input type="text" v-model="fullName">
  <p>Фамилия: {{lastName}}</p>
  <p>Имя: {{firstName}}</p>
  <p>Отчество: {{middleName}}</p>
  <button @click="splitName">Показать</button>
</template>

<style>

</style>