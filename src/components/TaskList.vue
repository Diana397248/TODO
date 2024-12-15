<script setup>
import TaskItem from '../components/TaskItem.vue';

const props = defineProps({
  todos: Array,
});
</script>

<template>
  <div class="list">
    <TaskItem v-for="todo in props.todos" :todo="todo"/>
    <h2> {{ todos }} </h2>

  </div>
</template>

<style scoped>
.list {
  padding: 10px;
  background-color: lightyellow;
}
</style>