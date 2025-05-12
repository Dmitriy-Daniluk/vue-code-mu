<template>
  <div>
    <UserForm @add="add" />
    <div v-for="user in users" :key="user.id">
      {{ user.name }} {{ user.surn }}
    </div>
  </div>
</template>

<script>
import UserForm from './components/UserForm.vue';

export default {
  components: {
    UserForm,
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
    add(name, surn) {
      let id = this.users.length + 1;
      this.users.push({
        id,
        name,
        surn,
      });
    },
  },
};
</script>
