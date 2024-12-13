<script setup>
import TaskItem from '../components/TaskItem.vue';

let todos = [{name: "постирать"}, {name: "сходить в магазин"}];
</script>

<template>
  <TaskItem v-for="todo in todos" :todo="todo"/>
</template>

<style scoped>

</style>