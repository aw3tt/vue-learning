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
   <Employee name="john" surn="smit" age="30"/>
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>