<script>
export default {
  props: {
    id: Number,
    name: String,
    salary: Number,
    age: Number,
    key: Number,
  },
  data() {
    return {

    }
  }
}
</script>
<template :key="key">
  <p>{{name}}</p>
  <p>{{salary}}</p>
  <p>{{age}}</p>
</template>