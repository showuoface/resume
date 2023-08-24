<template>
  <div
    class="academic"
    v-if="isMounted"
    v-bind:data-aos="'fade-up'"
    v-bind:data-aos-anchor-placement="'top-bottom'"
  >
    <div class="title">學歷.</div>
    <div class="detail">
      <p><strong>樹德科技大學</strong>的<strong>資訊工程系</strong>畢業</p>
    </div>
  </div>
</template>

<script lang="ts">
import { onMounted, ref } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";

export default {
  name: "AppAcademic",
  setup() {
    const isMounted = ref(false);

    onMounted(() => {
      AOS.init();
      isMounted.value = true;
    });

    return {
      isMounted,
    };
  },
};
</script>

<style scoped lang="scss">
.academic {
  z-index: 1;
  background-color: white;
  position: absolute;
  left: 0;
  width: 100%;
  padding: 60px 0;
  .title {
    font-size: 80px;
    margin-bottom: 60px;
  }
  .detail {
    margin: 0 auto;
    max-width: 500px;
    @media (max-width: 780px) {
      max-width: 400px;
    }
  }
}
</style>
