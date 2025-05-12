<template>
  <div>
    <Employee @action1="action1" @action2="action2" />
  </div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
  components: {
    Employee,
  },
  methods: {
    action1() {
      alert('Action 1 triggered!');
    },
    action2() {
      alert('Action 2 triggered!');
    },
  },
};
</script>