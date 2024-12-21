<script setup>
import TaskList from '../components/TaskList.vue';
import TaskForm from '../components/TaskForm.vue';
import {ref} from "vue";


const todos = ref([
  {id: 1, name: "постирать", completed: false},
  {id: 2, name: "сходить в магазин", completed: false}]);

let lastId = 2

const createTodo = (taskName) => {
  lastId += 1;
  let newTask = {id: lastId, name: taskName, completed: false}
  todos.value.push(newTask)
}

const changeTodo = (todo) => {
  todos.value
}
</script>

<template>
  <div class="page">
    <TaskList :todos="todos"/>
    <TaskForm :createTodo="createTodo"/>
  </div>
</template>

<style scoped>
.page {
  padding: 20px;
  background-color: lightgreen;
}
</style>