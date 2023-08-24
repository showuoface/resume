<template>
  <div
    class="about"
    v-if="isMounted"
    v-bind:data-aos="'fade-up'"
    v-bind:data-aos-anchor-placement="'top-bottom'"
  >
    <div class="title">About.</div>
    <div class="detail">
      <p>
        我叫做游永煌，也可以叫我Aleng或是游泳，畢業於<strong>樹德科技大學</strong>的<strong>資訊工程系</strong>大學專題主要是朝手機Android
        Studio與樹梅派的藍芽結合，專題名稱是<strong>車輛診斷系統連接音響</strong>，內容是使用OBD
        <span class="tip">(車輛診斷系統板子)</span>與手機還有樹梅派<span
          class="tip"
          >(這邊是音響)</span
        >利用藍芽進行連接還有資料上的轉換，使故障能夠在手機與藍芽上撥放與顯示。
        目前主要在前端開發上比較精進，且就職於<strong>資旅軟體開發有限公司</strong>。
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { onMounted, ref } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";

export default {
  name: "AppAbout",
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
.about {
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
    max-width: 700px;
    @media (max-width: 780px) {
      max-width: 400px;
    }
  }
}
</style>
