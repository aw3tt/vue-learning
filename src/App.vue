<script>
export default {
  data() {
    return {
      cost: 300,
      amount: 5
    }
  },
  methods: {
    show: function(number) {
      alert(this.square(number));
    },
    change: function(text) {
      this.text = text;
    }
  },
  computed: {
    price: function() {
      return this.cost * this.amount;
    }
  }
}
</script>

<template>
  <p>{{ cost }}</p>
  <p>{{ amount }}</p>
  <p>{{ price }}</p>
  <button @click="this.cost = 500">change</button>
</template>
