<template>
  <div class="background-image"></div>
</template>

<script lang="ts">
export default {
  name: "AppMedia2",
};
</script>

<style scoped lang="scss">
.background-image {
  background-image: url("../../assets/media2.png");
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: -2;
  left: 0;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
