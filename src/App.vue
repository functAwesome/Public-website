<template>
  <div id="app">
    <Navbar /> 
      <Banner />
      <hr>
      <Benefits />
      <hr>
      <Tokenomics />
      <hr>
      <Roadmap />
      <hr>
      <Team />
      <hr>
      <Faq />
      <Footer />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Navbar from './components/Navbar.vue';
import Banner from './components/Banner.vue'
import Roadmap from './components/Roadmap.vue'
import Tokenomics from './components/Tokenomics.vue'
import Footer from './components/Footer.vue'
import Benefits from './components/Benefits.vue'
import Team from './components/Team.vue'
import Faq from './components/Faq.vue'

@Component({
  components: {
    Navbar,
    Banner,
    Tokenomics,
    Benefits,
    Roadmap,
    Team,
    Faq,
    Footer
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
*{
  max-width: 100vw;
  overflow-x: hidden !important;
}
#app {
  font-family: Arial;
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
}
.section-heading{
  font-size: 25pt;
  text-decoration: underline;
  text-decoration-color: black;
  text-decoration-thickness: 5px;
  text-align: center;
  margin-bottom: 2rem;
  margin-top: 2rem;
}
.hover-blue:hover{
  color: rgb(20, 20, 50);
}
.text-white{
    color: white;
}
hr{
  background-color: rgb(223, 223, 223);
  height: 2px;
  border: none;
  margin: 0 auto;
  width: 40vw;
}
.my-margin{
  margin: 7em 0;
}
</style>
