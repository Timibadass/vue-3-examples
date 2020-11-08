<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Vue 3 is liveeeee!" />
    <select name="color" id="color" v-model="selectedColor">
      <option value="" disabled selected> Select a color</option>
      <option :value="color" v-for="(color, index) in colors" :key="index"
        >{{ color }}
      </option>
    </select>
    <video-player></video-player>
  </div>
</template>

<script>
  import HelloWorld from "@/components/HelloWorld.vue";
  import videoPlayer from "@/components/videoComponent.vue";
  import { computed } from "vue";

  export default {
    name: "Home",
    components: {
      HelloWorld,
      videoPlayer,
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
<style></style>
