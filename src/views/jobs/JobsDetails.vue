<template>
  <h1>{{ title }}</h1>
  <p>The job id is: {{ id }}</p>
</template>

<script>
export default {
  props: ["id", "title"],
  data() {
    return {};
  },
};
</script>

<style>
</style>