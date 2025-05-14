<script>
export default {
  data() {
    return {
      users: [
        {
          id: 1,
          name: 'name1',
          salary: 100,
          age: 30,
        },
        {
          id: 2,
          name: 'name2',
          salary: 200,
          age: 40,
        },
        {
          id: 3,
          name: 'name3',
          salary: 300,
          age: 50,
        },
      ],
    }
  },
  methods: {
    removeUser(userId) {
      // Удаляем пользователя по id
      this.users = this.users.filter(user => user.id !== userId);

      // Альтернативный вариант через индекс:
      // const index = this.users.findIndex(user => user.id === userId);
      // if (index !== -1) this.users.splice(index, 1);
    }
  }
}
</script>

<template>
  <div>
    <table>
      <thead>
      <tr>
        <th>ID</th>
        <th>Имя</th>
        <th>Зарплата</th>
        <th>Возраст</th>
        <th>Действия</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="user in users" :key="user.id">
        <td>{{ user.id }}</td>
        <td>{{ user.name }}</td>
        <td>{{ user.salary }}</td>
        <td>{{ user.age }}</td>
        <td>
          <a href="#" @click.prevent="removeUser(user.id)">Удалить</a>
        </td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>