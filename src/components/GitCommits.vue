<template>
  <div v-if="commits">
    <table class="table">
      <thead>
      <tr>
        <th scope="col">Author</th>
        <th>Commit Message</th>
        <th>Date</th>
        <th>URL</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="commit_data in commits" :key="commit_data">
        <th scope="row">{{commit_data.author.login}}</th>
        <td>{{commit_data.commit.message}}</td>
        <td>{{ commit_data.commit.author.date }}</td>
        <td><a target="_blank" :href="commit_data.html_url">View Commit</a></td>
      </tr>
      </tbody>
    </table>
  </div>
  <div v-else>
    <h3>No commits were found</h3>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: 'GitCommits',
  data(){
    return {
      commits : []
    }
  },
  mounted() {
    this.fetchData();
  },
  methods:{
    fetchData(){
      var self = this;
      axios.get('https://api.github.com/repos/mh-technologies/fetch-git-commits/commits')
        .then(function (response) {
          self.commits = response.data;
          console.log(response.data);
        })
        .catch(function () {

        })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
