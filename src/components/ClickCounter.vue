<template>
  <button class="btn btn-secondary" @click="incrementCounter">
    Clicked {{ counter }} times
  </button>
</template>

<script>
import CounterMixin from "../mixins/counter.js";
export default {
  name: "ClickCounter",
  mixins: [CounterMixin],
};
</script>

<style scoped>
</style>