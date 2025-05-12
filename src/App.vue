<template>
  <div>
    <Employee @sendName="func" @sendEmployee="funcWithSalary" />
  </div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
  components: {
    Employee,
  },
  methods: {
    // Метод для обработки имени работника
    func(name) {
      console.log(name);  // Выводим имя работника в консоль
    },

    // Метод для обработки имени и зарплаты работника
    funcWithSalary(name, salary) {
      console.log(name, salary);  // Выводим имя и зарплату работника в консоль
    },
  },
};
</script>