<template>
  <div>
    <div class="mb-3">
      <label for="example-input" class="form-label h4">Name</label>
      <input
        type="text"
        class="form-control form-control-lg"
        id="example-input"
        placeholder="Insert your name..."
        ref="nameInput"
      />
    </div>
    <posts-list ref="postsList" />
  </div>
</template>

<script>
import PostsList from "./PostsList.vue";
export default {
  name: "TemplateRef",
  components: {
    PostsList,
  },
  mounted() {
    this.$refs.nameInput.focus();
    console.log(this.$refs.postsList);
  },
};
</script>

<style scoped>
</style>