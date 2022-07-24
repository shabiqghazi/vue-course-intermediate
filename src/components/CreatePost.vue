<template>
  <h2>Create Post</h2>
  <form @submit.prevent="createPost">
    <div class="mb-3">
      <label for="title" class="form-label">Title</label>
      <input
        type="text"
        class="form-control"
        id="title"
        placeholder="Title..."
        v-model="postData.title"
      />
    </div>
    <div class="mb-3">
      <label for="body" class="form-label">Body</label>
      <textarea
        class="form-control"
        id="body"
        rows="3"
        v-model="postData.body"
      ></textarea>
    </div>
    <div class="mb-3">
      <label for="userId" class="form-label">User ID</label>
      <input
        type="text"
        class="form-control"
        id="userId"
        placeholder="User Id..."
        v-model="postData.userId"
      />
    </div>
    <div class="mb-">
      <button class="btn btn-primary">Submit</button>
    </div>
  </form>
</template>

<script>
import axios from "axios";
export default {
  name: "CreatePost",
  data() {
    return {
      postData: {
        title: "",
        body: "",
        userId: "",
      },
    };
  },
  methods: {
    createPost() {
      axios
        .post("https://jsonplaceholder.typicode.com/posts", this.postData)
        .then((res) => {
          console.log(res);
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>

<style scoped>
</style>