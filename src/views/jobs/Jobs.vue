<template>
  <h1>Job Offers</h1>
  <div class="jobs" v-for="job in jobs" v-bind:key="job.id">
    <router-link
      v-bind:to="{
        name: 'JobsDetails',
        params: { id: job.id, title: job.title },
      }"
      ><h2>{{ job.title }}</h2></router-link
    >
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          title: "UX Designer",
          id: 1,
          details:
            "orem ipsum dolor sit amet, consectetur adipiscing elit. Proin fermentum mauris quam. ",
        },
        {
          title: "Web Developer",
          id: 2,
          details:
            "orem ipsum dolor sit amet, consectetur adipiscing elit. Proin fermentum mauris quam. ",
        },
        {
          title: "DevOps Engineer",
          id: 3,
          details:
            "orem ipsum dolor sit amet, consectetur adipiscing elit. Proin fermentum mauris quam. ",
        },
      ],
    };
  },
};
</script>

<style>
</style>