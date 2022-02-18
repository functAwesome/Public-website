<template>
  <nav :class="{ 'onScroll': !topOfPage}">
    <div class="brand">
      <img class="brand-logo" src="@/assets/Logo.png" alt="">
      <div class="brand-text">YAMFORE</div>
    </div>
    <div class="flex-links" v-bind:class="{ open: isOpen }">
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>ABOUT</div></a>
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>TEAM</div></a>
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>WHITEPAPER</div></a>
    </div>
    <a class="to-app" href="https://app.yamfore.com">TO APP</a>
    <div
      class="hamburger"
      v-bind:class="{ toggle: isToggle }"
      @click="hamburgerClick()"
    >
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
    <div class="mobile-navbar">
      <div class="mobile-link"><a class="hover-blue" href="">ABOUT</a></div>
      <div class="mobile-link"><a class="hover-blue" href="">TEAM</a></div>
      <div class="mobile-link"><a class="hover-blue" href="">WHITEPAPER</a></div>
    </div>
  </nav>
</template>
<script>
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Navbar extends Vue {
  topOfPage = true;
  isOpen = false;
  isFade = false;
  isToggle = false;
  
  handleScroll(){
    console.log('scroll')
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
  mounted(){
    window.addEventListener('scroll', this.handleScroll)
  }
}
</script>
<style scoped lang="scss">
*{
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
nav{
  position: fixed;
  height: 6em;
  width: 100vw;
  background-color: transparent;
  z-index: 100;
  display: flex;
  justify-content: space-between;
  align-items: center;
  overflow-x: hidden;
  &.onScroll {
      box-shadow: 0 0 10px #aaa;
      background-color: #fff;
      ul li {
        color: #10b761;
      }
    }
}
.brand{
  margin-left: 5em;
  display: flex;
  align-items: center;
  padding: 0em 1em;
}
.brand-logo {
  height: 4rem;
  width: 4rem;
}
.brand-text{
  margin-left: 1em;
  font-size: 22pt;
}
/* Styling links */
.flex-links{
  padding-right: 30em;
  display: flex;
  align-items: center;
}
.links{
  list-style: none;
  text-decoration: none;
  margin: 0 1em;
  font-size: 15pt;
  color: black;
}
.to-app{
  text-decoration: none;
  color: white;
  background-color: /* rgb(18, 18, 170) */ #162d5d
  /* rgb(23, 110, 222)
  rgb(20, 20, 50); */;
  border-radius: 5px;
  padding: 0.7em;
  margin-right: 10em;
  
}
/*Styling Hamburger Icon*/
.hamburger div {
  width: 30px;
  height: 3px;
  background: #551a8b;
  margin: 5px;
  transition: all 0.3s ease;
}
.hamburger {
  display: none;
}
/*Animating Hamburger Icon on Click*/
.toggle .line1 {
  transform: rotate(-45deg) translate(-5px, 6px);
}
.toggle .line2 {
  transition: all 0.7s ease;
  width: 0;
}
.toggle .line3 {
  transform: rotate(45deg) translate(-5px, -6px);
}
/* Mobile navbar */
.mobile-navbar{
  display: none;
}
/* Media */
@media screen and (max-width: 800px) {
  .hamburger {
    display: block;
    position: absolute;
    cursor: pointer;
    right: 5%;
    top: 50%;
    transform: translate(-5%, -50%);
    z-index: 2;
    transition: all 0.7s ease;
  }
  .mobile-navbar{
    position: absolute;
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .flex-links {
    background: #f2f5f7;
    height: 100vh;
    width: 100%;
    flex-direction: column;
    clip-path: circle(50px at 90% -20%);
    -webkit-clip-path: circle(50px at 90% -10%);
    transition: all 1s ease-out;
    pointer-events: none;
  }
  .flex-links.open {
    width: 100vw !important;
    height: 100% !important;
    clip-path: circle(1500px at 90% -10%);
    -webkit-clip-path: circle(1500px at 90% -10%);
    pointer-events: all;
  }
  .flex-links div {
    opacity: 0;
  }
  .flex-links div:nth-child(1) {
    transition: all 0.5s ease 0.2s;
  }
  .flex-links div:nth-child(2) {
    transition: all 0.5s ease 0.4s;
  }
  .flex-links div:nth-child(3) {
    transition: all 0.5s ease 0.6s;
  }
  .flex-links div:nth-child(4) {
    transition: all 0.5s ease 0.7s;
  }
  .flex-links div.fade {
    opacity: 1;
  }
}
</style>
