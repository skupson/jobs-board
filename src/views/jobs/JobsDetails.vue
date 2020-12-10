<template>
  <div class="job" v-if="job">
    <h1>{{ job.title }}</h1>
    <h2>The job id is: {{ job.id }}</h2>
    <p>{{ job.details }}</p>
  </div>
</template>

<script>
export default {
  props: ["id"],
  mounted() {
    fetch(`http://localhost:3000/jobs/${this.id}`)
      .then((res) => res.json())
      .then((data) => (this.job = data))
      .catch((err) => console.log("Error getting the data"));
  },
  data() {
    return {
      job: null,
    };
  },
};
</script>

<style>
</style>