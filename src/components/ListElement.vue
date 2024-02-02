<script setup>
import { ref, computed } from 'vue'

// give each todo a unique id
let id = 0

const newTodo = ref('')
const todos = ref([
  { id: id++, text: 'Learn HTML', done: false },
  { id: id++, text: 'Learn JavaScript', done: false },
  { id: id++, text: 'Learn Vue', done: false }
])
const hideCompleted = ref(false);

const filteredTodos = computed(() => {
  if (hideCompleted.value) {
    return todos.value.filter(todo => !todo.done)
  } else {
    return todos.value
  }
})
function addTodo() {
  todos.value.push({
    id: id++,
    text: newTodo.value
  })
  newTodo.value = ''
}
function hideCompletedItems() {
  hideCompleted.value = !hideCompleted.value;
}

function removeTodo(todo) {
  // ...
}
</script>

<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo">
    <button>Add Todo</button>    
  </form>
  <ul>
    <li v-for="todo in filteredTodos" :key="todo.id">
      <input type="checkbox" v-model="todo.done">
      {{ todo.text }}
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
  <button @click="hideCompletedItems">
  {{ !hideCompleted ? "Hide Completed Tasks" : "Show Completed Tasks" }}
  </button>
</template>
