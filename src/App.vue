<template>
  <div id="app">
    <Navbar /> 
    
      <Banner />
      <About/>
      <Roadmap />
      <Footer />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Navbar from './components/Navbar.vue';
import Banner from './components/Banner.vue'
import About from './components/About.vue'
import Roadmap from './components/Roadmap.vue'
import Footer from './components/Footer.vue'

@Component({
  components: {
    Navbar,
    Banner,
    About,
    Roadmap,
    Footer
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
*{
  max-width: 100vw;
  overflow-x: hidden;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0;
  padding: 0;
}
.section{
  position:relative;
  width: 100vw !important;
  height: auto;
  overflow-x: hidden;
  margin-bottom: 1em;
}
.section-heading{
  font-size: 20pt;
  text-decoration: underline;
  text-align: center;
  margin-bottom: 2rem;
  margin-top: 2rem;
}
.hover-blue:hover{
  color: rgb(20, 20, 50);
}
</style>
