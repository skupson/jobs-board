<template>
  <h1>Job Offers</h1>
  <div class="jobs" v-for="job in jobs" v-bind:key="job.id">
    <router-link
      v-bind:to="{
        name: 'JobsDetails',
        params: { id: job.id },
      }"
      ><h2>{{ job.title }}</h2></router-link
    >
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [],
    };
  },
  mounted() {
    fetch("http://localhost:3000/jobs")
      .then((res) => res.json())
      .then((data) => (this.jobs = data))
      .catch((err) => console.log("Error getting the data"));
  },
};
</script>

<style>
</style>