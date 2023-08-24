<template>
  <div class="backgroundVideo">
    <video
      ref="videoElement"
      src="../../assets/background-video.mp4"
      autoplay
      muted
      loop
    ></video>
  </div>
</template>

<script lang="ts">
export default {
  name: "AppBackground",
};
</script>

<style scoped lang="scss">
.backgroundVideo {
  position: absolute;
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  opacity: 1;
  overflow: hidden;
  z-index: -3;
  video {
    width: 100%;
    height: 140%;
    object-fit: cover;
  }
}
</style>
