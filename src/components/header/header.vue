<template>
  <div class="header">
    <img src="../../assets/person-image.png" />
    <div class="headerDetail">
      <div class="headerName">
        <span class="headerNameTC_name">游永煌</span>
        <span class="headerNameDividing">/</span>
        <span class="headerNameEN_name">Aleng</span>
      </div>
      <div class="headerIcon">
        <a
          href="https://www.facebook.com/profile.php?id=100007650403949"
          target="_blank"
        >
          <i class="fa-brands fa-facebook fa-2xl"></i>
        </a>
        <a href="https://www.instagram.com/aleng_085/" target="_blank">
          <i class="fa-brands fa-instagram fa-2xl"></i>
        </a>
        <a href="mailto:aleng@webglsoft.com">
          <i class="fa-solid fa-envelope fa-2xl"></i>
        </a>
      </div>
      <div class="headerTitle">FrontEnd Engineer</div>
    </div>
    <div class="headerMenu">
      <Swiper
        v-if="isWideScreen"
        v-bind="swiperOptions"
        :slides-per-view="3"
        :space-between="50"
      >
        <SwiperSlide
          v-for="(item, index) in items"
          :key="index"
          @click="handleSlideClick(item.key)"
        >
          {{ item.value }}
        </SwiperSlide>
      </Swiper>
    </div>
  </div>
</template>

<script lang="ts">
import { ref, onMounted, onBeforeUnmount } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  name: "AppHeader",
  setup() {
    const items = [
      { key: "about", value: "About." },
      { key: "academic", value: "學歷." },
      { key: "experience", value: "Experience." },
      { key: "tne", value: "Technology. & Expertise." },
      { key: "project", value: "Project." },
      { key: "contact", value: "Contact." },
    ];
    const swiperOptions = {
      slidesPerView: 3,
      loop: true,
      centeredSlides: true,
      noSwipingClass: "no-swiping",
    };
    const isWideScreen = ref(false);

    const updateScreenSize = () => {
      isWideScreen.value = window.innerWidth >= 768;
    };

    onMounted(() => {
      updateScreenSize();
      window.addEventListener("resize", updateScreenSize);
    });

    onBeforeUnmount(() => {
      window.removeEventListener("resize", updateScreenSize);
    });

    const handleSlideClick = (key: string) => {
      const element = document.querySelector(`.${key}`);
      if (element) {
        const offsetTop = (element as HTMLElement).offsetTop;
        const elementHeight = element.clientHeight;
        const windowHeight = window.innerHeight;
        const scrollToPosition = offsetTop - (windowHeight - elementHeight) / 2;
        window.scrollTo({ top: scrollToPosition, behavior: "smooth" });
      }
    };

    return {
      items,
      isWideScreen,
      swiperOptions,
      handleSlideClick,
    };
  },
};
</script>

<style scoped lang="scss">
.header {
  margin-bottom: 510px;
  img {
    height: 250px;
    width: 250px;
    border-radius: 50%;
    overflow: hidden;
  }
  .headerDetail {
    .headerName {
      margin: 20px 0;
      font-size: 25px;
      font-weight: bold;
      .headerNameDividing {
        margin: 0 10px;
      }
    }
    .headerIcon {
      margin: 20px 0;
      a {
        color: gray;
        margin: 0 10px;
      }
    }
    .headerTitle {
      font-size: 30px;
      font-weight: bold;
    }
  }
  .headerMenu {
    margin-top: 70px;
    .swiper {
      width: 70%;
      .no-swiping {
        pointer-events: none;
      }
      .swiper-slide {
        cursor: pointer;
        font-size: 35px;
        font-weight: bold;
        transition: color 0.8s;
        &:hover {
          color: rgb(195, 19, 19);
        }
      }
    }
    .menu-item {
      padding: 20px;
      border-bottom: 1px solid #ddd;
      cursor: pointer;
    }
  }
}
</style>
