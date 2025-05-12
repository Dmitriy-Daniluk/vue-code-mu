<template>
  <div>
    <Employee
      v-for="user in users"
      :key="user.id"
      :id="user.id"
      :name="user.name"
      :surn="user.surn"
      @remove="remove"
    />
  </div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
  components: {
    Employee,
  },
  data() {
    return {
      users: [
        { id: 1, name: 'name1', surn: 'surn1' },
        { id: 2, name: 'name2', surn: 'surn2' },
        { id: 3, name: 'name3', surn: 'surn3' },
      ],
    };
  },
  methods: {
    remove(id) {
      this.users = this.users.filter((user) => user.id !== id);
    },
  },
};
</script>
