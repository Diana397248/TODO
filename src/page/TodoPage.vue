<script setup>
import TaskList from '../components/TaskList.vue';
import TaskForm from '../components/TaskForm.vue';
import {ref} from "vue";

const todos = ref([{
  name: "постирать", type: false
}, {name: "сходить в магазин", type: false}]);

const createTodo = (taskName) => {
  let newTask = {name: taskName, type: false}
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