<script>
export default {
  data() {
    return {
      products: [
        {
          name: 'product1',
          price: 100,
          quantity: 5
        },
        {
          name: 'product2',
          price: 200,
          quantity: 4
        },
        {
          name: 'product3',
          price: 300,
          quantity: 3
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
  <ul>
    <template v-for="ref in hrefs">
      <li>
        <a :href="ref.href">{{ref.text}}</a>
      </li>
    </template>
  </ul>

  <table>
    <template v-for="product in products">
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.price}}</td>
        <td>{{product.quantity}}</td>
      </tr>
    </template>
  </table>
</template>
