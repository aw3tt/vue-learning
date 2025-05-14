<script>
import Employee from './components/Employee.vue'
export default {
  components: {
    Employee
  },

  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<template>
  <div>
   <Employee :arg="[1, 2, 3]"/>
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>