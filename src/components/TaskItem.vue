<script setup>

const props = defineProps({
  todo: Object,
});

</script>

<template>
  <h2> {{ props.todo.name }} </h2>
</template>

<style scoped>

</style>