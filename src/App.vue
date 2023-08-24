<template>
  <Layout />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Layout from "./components/index.vue";

@Options({
  components: {
    Layout,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
body {
  margin: 0;
}
#app {
  font-family: HelveticaNeue, Helvetica Neue, helvetica, Sans-Serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 30px;
}
</style>
