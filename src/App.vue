<script>
import Employee from './components/Employee.vue'
import EmployeeForm from "@/components/EmployeeForm.vue";
export default {
  components: {
    EmployeeForm,
    Employee
  },

  data() {
    return {
      users: [
        {
          id: 1,
          name: 'name1',
          surn: 'surn1'
        },
        {
          id: 2,
          name: 'name2',
          surn: 'surn2'
        },
        {
          id: 3,
          name: 'name3',
          surn: 'surn3'
        },
      ],
    }
  },
  methods: {
    change(id, name, surn) {
      this.users = this.users.map((user) => {
        if (user.id === id) {
          user.name = name;
          user.surn = surn;
        }
        return user;
      });
    },
    add(name, surn) {
      let id = this.users.length + 1;

      this.users.push({
        id,
        name,
        surn
      });
    }
  }
}
</script>

<template>
  <div>
   <Employee v-for="user in users" :key="user.id" :id="user.id" :name="user.name" :surn="user.surn" @change="change" />
    <EmployeeForm @add="add" />
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>