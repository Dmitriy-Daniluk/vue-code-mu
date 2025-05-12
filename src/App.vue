<template>
  <div>
    <h1>Чеклист</h1>
    <TodoForm @add="addTodo" />
    <ul>
      <li v-for="(todo, index) in todos" :key="todo.id" :class="{ completed: todo.completed }">
        <span v-if="!todo.isEdit" @click="toggleComplete(todo.id)">
          {{ todo.text }}
        </span>
        <input v-if="todo.isEdit" v-model="todo.newText" />
        <button @click="remove(todo.id)">Удалить</button>
        <button @click="edit(todo.id)">{{ todo.isEdit ? 'Сохранить' : 'Редактировать' }}</button>
      </li>
    </ul>
  </div>
</template>

<script>
import TodoForm from './components/TodoForm.vue';

export default {
  components: {
    TodoForm,
  },
  data() {
    return {
      todos: [],
    };
  },
  methods: {
    addTodo(text) {
      const newTodo = {
        id: Date.now(),
        text,
        completed: false,
        isEdit: false,
        newText: text,
      };
      this.todos.push(newTodo);
    },
    remove(id) {
      this.todos = this.todos.filter(todo => todo.id !== id);
    },
    toggleComplete(id) {
      const todo = this.todos.find(todo => todo.id === id);
      if (todo) {
        todo.completed = !todo.completed;
      }
    },
    edit(id) {
      const todo = this.todos.find(todo => todo.id === id);
      if (todo) {
        if (todo.isEdit) {
          todo.text = todo.newText;
        }
        todo.isEdit = !todo.isEdit;
      }
    },
  },
};
</script>

<style>
.completed {
  text-decoration: line-through;
}
</style>
