<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 }
      ],
      editingId: null,
      editForm: {
        name: '',
        salary: '',
        age: ''
      }
    }
  },
  methods: {
    removeUser(userId) {
      this.users = this.users.filter(user => user.id !== userId);
    },
    startEdit(user) {
      this.editingId = user.id;
      this.editForm = { ...user };
    },
    saveEdit() {
      const index = this.users.findIndex(user => user.id === this.editingId);
      if (index !== -1) {
        this.users[index] = { ...this.editForm };
      }
      this.cancelEdit();
    },
    cancelEdit() {
      this.editingId = null;
      this.editForm = { name: '', salary: '', age: '' };
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


        <td v-if="editingId === user.id">
          <input v-model="editForm.name" type="text">
        </td>
        <td v-else>{{ user.name }}</td>

        <td v-if="editingId === user.id">
          <input v-model.number="editForm.salary" type="number">
        </td>
        <td v-else>{{ user.salary }}</td>

        <td v-if="editingId === user.id">
          <input v-model.number="editForm.age" type="number">
        </td>
        <td v-else>{{ user.age }}</td>

        <td>
          <template v-if="editingId === user.id">
            <button @click="saveEdit">Сохранить</button>
            <button @click="cancelEdit">Отмена</button>
          </template>

          <template v-else>
            <a href="#" @click.prevent="startEdit(user)">Редактировать</a> |
            <a href="#" @click.prevent="removeUser(user.id)">Удалить</a>
          </template>
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