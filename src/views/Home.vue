<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Vue 3 is liveeeee!" />
    <select name="color" id="color" v-model="selectedColor">
      <option value="" disabled selected> Select a color</option>
      <option :value="color" v-for="(color, index) in colors" :key="index">{{
        color
      }}</option></select
    >
  </div>
</template>

<script>
  import HelloWorld from "@/components/HelloWorld.vue";
  import { computed } from "vue";

  export default {
    name: "Home",
    components: {
      HelloWorld,
    },
    data() {
      return {
        selectedColor: "",
        todos: ["Feed a cat", "Buy tickets"],
        colors: ["red", "blue", "green"],
      };
    },
    provide() {
      return {
        color: computed(() => this.selectedColor),
      };
    },
  };
</script>
