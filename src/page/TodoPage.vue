<script setup>
import TaskList from '../components/TaskList.vue';
import TaskForm from '../components/TaskForm.vue';
import {ref} from "vue";

const todos = ref([{name: "постирать"}, {name: "сходить в магазин"}]);

const createTodo = (taskName) => {
  let newTask = {name: taskName}
  todos.value.push(newTask)
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