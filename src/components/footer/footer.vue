<template>
  <div class="footer contact">
    <a
      href="https://www.facebook.com/profile.php?id=100007650403949"
      target="_blank"
    >
      <i class="fa-regular fa-copyright"></i>
      <span>for Aleng</span>
    </a>
  </div>
</template>

<script lang="ts">
export default {
  name: "AppFooter",
};
</script>

<style scoped lang="scss">
.footer {
  cursor: pointer;
  z-index: 1;
  position: absolute;
  width: 100%;
  padding: 10px 0;
  text-align: center;
  background-color: rgb(171, 64, 18);
  color: white;
  a {
    text-decoration: none;
    color: white;
    span {
      margin: 0 15px;
    }
  }
}
</style>
