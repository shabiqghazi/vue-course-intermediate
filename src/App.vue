<template>
  <div class="container">
    <div class="row">
      <div class="col-6">
        <posts-list />
      </div>
      <div class="col-6">
        <create-post />
      </div>
    </div>
  </div>
</template>

<script>
import PostsList from "./components/PostsList.vue";
import CreatePost from "./components/CreatePost.vue";
export default {
  name: "App",
  components: {
    PostsList,
    CreatePost,
  },
};
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
