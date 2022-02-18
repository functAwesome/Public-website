<template>
  <nav :class="{ 'onScroll': !topOfPage}">
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
  topOfPage = true;
  isOpen = false;
  isFade = false;
  isToggle = false;
  
  handleScroll(){
      if(window.pageYOffset>0){
        if(this.topOfPage) this.topOfPage = false
      } else {
        if(!this.topOfPage) this.topOfPage = true
      }
    }
    hamburgerClick() {
      if (this.isToggle === false) {
        this.isOpen = true;
        this.isFade = true;
        this.isToggle = true;
      } else {
        this.isOpen = false;
        this.isFade = false;
        this.isToggle = false;
      }
    }
  test = (): void => {
    console.log('this is test and called');
  };
  mounted(){
    window.addEventListener('scroll', this.handleScroll)
  }
}
  
</script>

<style scoped lang="scss">
  nav {
    position: fixed;
    width: 100%;
    height: 70px;
    background-color: transparent;
    display: flex;
    align-items: center;
    transition: all .2s ease-in-out;
    z-index: 100;
    &.onScroll {
      box-shadow: 0 0 10px #aaa;
      background-color: #fff;
      ul li {
        color: #10b761;
      }
    }
    ul {
      margin-left: 3em;
      width: 25%;
      display: flex;
      justify-content: space-between;

      li {
        cursor: pointer;
        font-weight: 600;
        list-style-type: none;
        color: black;
      }
    }
    toApp {
      right: 20px;
    }
  }
</style>
