<script>
import Employee from './components/Employee.vue'
export default {
  components: {
    Employee
  },

  data() {
    return {
      name: '',
      salary: 150000,
      age: 23,
    }
  },
  methods: {

  }
}
</script>

<template>
  <div>
   <Employee :name="name" :salary="salary" :age="age" />
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>