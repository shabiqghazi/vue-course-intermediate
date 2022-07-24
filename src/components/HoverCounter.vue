<template>
  <h2 @mouseover="incrementCounter">Hovered {{ counter }} times</h2>
</template>

<script>
import CounterMixin from "../mixins/counter.js";

export default {
  name: "HoverCounter",
  mixins: [CounterMixin],
};
</script>

<style scoped>
</style>