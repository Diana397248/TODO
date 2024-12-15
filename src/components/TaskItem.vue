<script setup>

const props = defineProps({
  todo: Object,
});

const changeType = (todo) => {
  todo.type = !todo.type;
};
</script>

<template>
  <div class="task">
    <input type="checkbox"
           :checked="props.todo.type"
           @change="changeType(props.todo)"
    />
    <h2> {{ props.todo.name }} </h2>
    <h2> {{ todo }} </h2>
  </div>
</template>

<style scoped>
.task {
  background-color: lightgray;
  display: flex;
}
</style>