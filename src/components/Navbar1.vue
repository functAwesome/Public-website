<template>
  <nav >
    <ul>
      <li><div class="logo"></div></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Team</a></li>
      <li><a href="https://gitbook.com">Whitepaper</a></li>
    </ul>
    <div
      class="hamburger"
      v-bind:class="{ toggle: isToggle }"
      @click="hamburgerClick()"
    >
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
    <button class="toApp"><a href="http://app.yamfore.com" target="_blank" rel="noopener noreferrer">GO TO APP</a></button>
  </nav>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Navbar extends Vue {
  
}
  
</script>

<style scoped lang="scss">
  
</style>
