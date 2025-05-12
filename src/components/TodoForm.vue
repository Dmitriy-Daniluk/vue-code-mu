<template>
  <div>
    <input v-model="newTodo" placeholder="Введите новое дело" />
    <button @click="saveTodo">Добавить</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodo: '',
    };
  },
  methods: {
    saveTodo() {
      if (this.newTodo) {
        this.$emit('add', this.newTodo);
        this.newTodo = '';
      }
    },
  },
};
</script>
