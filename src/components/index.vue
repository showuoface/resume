<template>
  <Background />
  <Header />
  <About />
  <div class="media1-container1">
    <Media1 />
  </div>
  <Academic />
  <div class="media1-container2">
    <Media1 />
  </div>
  <ExperienceAndTne />
  <div class="media1-container2">
    <Media2 />
  </div>
  <Project />
  <Footer />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Background from "./background/background.vue";
import Header from "./header/header.vue";
import About from "./about/about.vue";
import Media1 from "./background/media1.vue";
import Media2 from "./background/media2.vue";
import Academic from "./academic/academic.vue";
import ExperienceAndTne from "./experienceAndTne/experienceAndTne.vue";
import Project from "./project/project.vue";
import Footer from "./footer/footer.vue";

@Options({
  components: {
    Background,
    Header,
    About,
    Media1,
    Media2,
    Academic,
    ExperienceAndTne,
    Project,
    Footer,
  },
})
export default class AppIndex extends Vue {
  mounted() {
    window.scrollTo({ top: 0, behavior: "auto" });
  }
}
</script>

<style scoped lang="scss">
.media1-container1 {
  position: relative;
  height: 70vh;
}
.media1-container2 {
  position: relative;
  height: 100vh;
}
</style>
