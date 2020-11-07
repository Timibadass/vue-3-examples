<template>
  <p :class="[color.value]">This is an example of deeply nested props!</p>
</template>

<script>
  export default {
    inject: ["color"],
  };
</script>

<style>
  .blue {
    color: blue;
  }
  .red {
    color: red;
  }
  .green {
    color: green;
  }
</style>
