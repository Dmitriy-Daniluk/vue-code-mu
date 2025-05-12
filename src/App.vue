<template>
  <table>
    <thead>
      <tr>
        <th>Name</th>
        <th>Salary</th>
        <th>Age</th>
        <th>Actions</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="user in users" :key="user.id">
        <td>{{ user.name }}</td>
        <td>{{ user.salary }}</td>
        <td>{{ user.age }}</td>
        <td><a href="#" @click="removeItem(user.id)">Remove</a></td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 },
      ],
    };
  },
  methods: {
    removeItem(id) {
      this.users = this.users.filter(user => user.id !== id);
    },
  },
};
</script>
