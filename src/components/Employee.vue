<template>
  <div>
    <button @click="sendEmployeeName">Send Employee Name</button>
    <button @click="sendEmployeeDetails">Send Employee Details</button>
  </div>
</template>

<script>
export default {
  emits: ['sendName', 'sendEmployee'],
  methods: {
    // Отправляем только имя работника
    sendEmployeeName() {
      this.$emit('sendName', 'John Doe');  // Передаем имя работника
    },

    // Отправляем имя и зарплату работника
    sendEmployeeDetails() {
      this.$emit('sendEmployee', 'John Doe', 50000);  // Передаем имя и зарплату работника
    },
  },
};
</script>