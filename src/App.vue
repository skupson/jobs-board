<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
    <router-link v-bind:to="{ name: 'About' }">About</router-link>
    <router-link v-bind:to="{ name: 'Jobs' }">Jobs</router-link>
  </div>
  <router-view />
</template>

<style>
</style>
