<template>
  <teleport :to="teleport" :disabled="minimizeVideo">
    <video src="../assets/00c3764e-aa4c-4d96-b9d9-b9a1d9c910e3.mp4"></video>
    <button @click="activateTeleport">Activate</button>
    <button @click="switchPosition">switch postion</button>
  </teleport>
</template>

<script>
  export default {
    data() {
      return {
        minimizeVideo: true,
        teleport: "footer",
      };
    },
    methods: {
      activateTeleport() {
        this.minimizeVideo = !this.minimizeVideo;
      },
      switchPosition() {
        this.teleport === ".header"
          ? (this.teleport = "footer")
          : (this.teleport = ".header");
      },
    },
  };
</script>

<style>
  video {
    width: 300px;
    height: 300px;
  }
</style>
