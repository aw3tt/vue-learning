<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'product1',
        },
        {
          id: 2,
          name: 'product2',
        },
        {
          id: 3,
          name: 'product3',
        },
      ]
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <ul v-for="product in products" :key="product.id">
    <li>{{product.name}}</li>
  </ul>
</template>
