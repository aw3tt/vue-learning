<script>
export default {
  data() {
    return {
      num1: 1,
      num2: 2,
    }
  },
  methods: {
    show: function(number) {
      alert(this.square(number));
    },
    square: function(number) {
      return Math.pow(number, 2);
    }
  }
}
</script>

<template>
  <button @click="show(2)">btn1</button>
  <button @click="show(3)">btn2</button>
</template>
