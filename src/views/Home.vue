<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <!-- <HelloWorld msg="Vue 3 is liveeeee!" /> -->
    <!-- <select name="color" id="color" v-model="selectedColor">
      <option value="" disabled selected> Select a color</option>
      <option :value="color" v-for="(color, index) in colors" :key="index"
        >{{ color }}
      </option>
    </select>
    <video-player></video-player> -->
    <div>
      <input-component
        class="awesome__class"
        label="name"
        type="text"
      ></input-component>
    </div>
  </div>
</template>

<script>
  // import HelloWorld from "@/components/HelloWorld.vue";
  // import videoPlayer from "@/components/videoComponent.vue";
  import inputComponent from "../components/input.vue";
  import { computed } from "vue";

  export default {
    name: "Home",
    components: {
      // HelloWorld,
      // videoPlayer,
      inputComponent,
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
<style>
  .awesome__class {
    border: 1px solid red;
  }
</style>
