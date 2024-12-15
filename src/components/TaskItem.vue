<script setup>

const props = defineProps({
  todo: Object,
});

const changeCompletedHandler = (todo) => {
  todo.type = !todo.type;
};
</script>

<template>
  <div class="task">
    <input type="checkbox"
           :checked="props.todo.type"
           @change="changeCompletedHandler(props.todo)"
    />
    <h2> {{ props.todo.name }} </h2>
  </div>
</template>

<style scoped>
.task {
  background-color: lightgray;
  display: flex;
}
</style>