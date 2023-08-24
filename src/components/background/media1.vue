<template>
  <div class="background1-image"></div>
</template>

<script lang="ts">
export default {
  name: "AppMedia",
};
</script>

<style scoped lang="scss">
.background1-image {
  background-image: url("../../assets/media1.png");
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
