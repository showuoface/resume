<template>
  <div class="project">
    <div class="title">Projects.</div>
    <div class="detail">
      <p>目前尚無拿的出手的作品集，待更新...</p>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "AppProject",
};
</script>

<style scoped lang="scss">
.project {
  z-index: 1;
  background-color: white;
  position: absolute;
  left: 0;
  width: 100%;
  padding: 60px 0;
  min-height: 500px;
  .title {
    font-size: 80px;
    margin-bottom: 60px;
  }
  .detail {
    margin: 0 auto;
    max-width: 700px;
  }
}
</style>
