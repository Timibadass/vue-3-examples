<template>
  <teleport to="header">
    <h1 class="logo">Vue 3 🥳</h1>
    <nav>
      <router-link to="/">Home</router-link>
    </nav>
  </teleport>
</template>

<script>
  export default {
    name: "app-header",
  };
</script>

<style>
  .header {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .logo {
    margin-right: 20px;
  }
</style>
