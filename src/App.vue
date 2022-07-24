<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-6">
        <!-- <div class="col-6">
        <posts-list />
      </div>
      <div class="col-6">
        <create-post />
      </div>
      <parent-component /> -->
        <!-- <template-ref /> -->
        <click-counter />
        <hover-counter />
      </div>
    </div>
  </div>
</template>

<script>
// import PostsList from "./components/PostsList.vue";
// import CreatePost from "./components/CreatePost.vue";
// import ParentComponent from "./components/Parent.vue";
// import TemplateRef from "./components/TemplateRef.vue";
import ClickCounter from "./components/ClickCounter.vue";
import HoverCounter from "./components/HoverCounter.vue";
export default {
  name: "App",
  components: {
    // PostsList,
    // CreatePost,
    // ParentComponent,
    // TemplateRef,
    ClickCounter,
    HoverCounter,
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
