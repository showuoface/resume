<template>
  <div class="experience tne" data-aos="fade-up">
    <div class="title">
      <p>工作經驗 & 技能</p>
    </div>
    <div class="detail">
      <p>
        大學實習於鈦昇科技公司，職位為機台設定人員，主要工作是設定及初始化機台設備，需同時了解硬體與軟體之間的原理。
      </p>
      <p>
        現在就業於資旅軟體開發有限公司，擔任前端工程師，使用到的技能有Angular前端框架、前端Framework、Impex、SAP系統、TypeScript、Sass/Scss、HTML5
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { onMounted, ref } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";

export default {
  name: "AppExperienceAndTne",
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
.experience {
  z-index: 1;
  background-color: white;
  position: absolute;
  left: 0;
  width: 100%;
  padding: 60px 0;
  .title {
    width: 100%;
    font-size: 80px;
    margin-bottom: 60px;
    p {
      @media (max-width: 780px) {
        max-width: 350px;
      }
      margin: 0 auto;
    }
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
