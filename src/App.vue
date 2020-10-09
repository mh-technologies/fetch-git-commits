<template>
  <h1>Fetching Git Commits</h1>
  <GitCommits></GitCommits>
</template>

<script>
import GitCommits from './components/GitCommits.vue'
// const Vue = window.vue;
// import axios from "axios";

export default {
  name: 'App',
  components: {
    GitCommits
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
