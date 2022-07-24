<template>
  <button class="btn btn-secondary mb-2" @click="loadPosts">Load Posts</button>
  <div class="alert alert-danger mb-4" role="alert" v-if="errMsg">
    {{ errMsg }}
  </div>
  <div class="card mb-2" v-for="post in posts" :key="post.id">
    <div class="card-header">
      <div class="card-title">#{{ post.id }} {{ post.title }}</div>
    </div>
    <div class="card-body">
      {{ post.body }}
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "PostsList",
  data() {
    return {
      posts: [],
      errMsg: "",
    };
  },
  methods: {
    loadPosts() {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((res) => {
          this.posts = res.data;
        })
        .catch((err) => {
          this.errMsg = err.message;
        });
    },
  },
  created() {
    this.loadPosts();
  },
};
</script>

<style scoped>
</style>