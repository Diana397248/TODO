<script setup>

const props = defineProps({
  todo: Object,
});

</script>

<template>
  <div class="task">
    <h2> {{ props.todo.name }} </h2>
  </div>
</template>

<style scoped>
.task {
  background-color: lightgray;
}
</style>