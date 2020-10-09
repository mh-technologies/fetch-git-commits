<template>
  <h1>Fetching Git Commits For Repo "fetch-git-commits"</h1>
  <p>Simple application for fetching the commits message and commit URLs.</p>
  <GitCommits></GitCommits>
</template>

<script>
import GitCommits from './components/GitCommits.vue'

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
