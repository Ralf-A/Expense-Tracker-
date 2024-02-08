
<script>
import { RouterLink, RouterView } from 'vue-router'
import Header from "@/components/Header.vue";


export default {
  name: 'App',
  components: {
    Header,
  },
  mounted() {
    this.logMountedComponent();
  },
  methods: {
    logMountedComponent() {
      console.log('App component mounted');
    },
  },
};
</script>

<template>
  <div id="app">
    <div class="content">
      <Header />
      <router-view />
    </div>
  </div>
</template>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  min-height: 100vh;
  min-width: 100vh;
    text-align: center;
    line-height: normal;
    text-align: center;
    font-family: 'Inter', sans-serif;


}


@media (min-width: 1024px) {
  #app {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    display: flex;
    min-height: 100vh;
    min-width: 100vh;

  }
}
</style>
