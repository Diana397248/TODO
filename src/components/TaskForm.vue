<script setup>
import {ref} from "vue";

const props = defineProps({
  createTodo: Function,
});

const nameTask = ref("")

const createFormHandler = () => {
  props.createTodo(nameTask.value);
  nameTask.value = '';
}

</script>

<template>
  <div class="form">
    <input type="text" v-model="nameTask"/>
    <button @click="createFormHandler">Добавить</button>
  </div>
</template>

<style scoped>
.form {
  margin: 10px;
  padding: 10px;
  background-color: lightblue;
}
</style>