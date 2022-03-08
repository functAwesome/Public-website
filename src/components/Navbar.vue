<template>
  <nav :class="{ 'onScroll': !topOfPage}">
    <div class="brand">
      <img class="brand-logo" src="@/assets/Logo.png" alt="">
      <div class="brand-text">YAMFORE</div>
    </div>
    <div class="flex-links" v-bind:class="{ open: isOpen }">
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>TOKENOMICS</div></a>
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>ROADMAP</div></a>
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>TEAM</div></a>
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>LITEPAPER</div></a>
      <a @click="expand()" class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>COMMUNITY</div></a><div class="community">hello</div>
      <a class="links hover-blue" v-bind:class="{ fade: isFade }" href=""><div>FAQ</div></a>
    </div>
    <a class="to-app" href="https://app.yamfore.com">LAUNCH</a>
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
      <div class="mobile-link"><a class="hover-blue" href="">LITEPAPER</a></div>
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
  isExpand = false;
  
  handleScroll(){
    console.log('scroll')
      if(window.pageYOffset>0){
        if(this.topOfPage) this.topOfPage = false
      } else {
        if(!this.topOfPage) this.topOfPage = true
      }
    }
    expand(){
      this.isExpand = true
      console.log(this.isExpand)
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
  width: fit-content;
}
.brand-logo {
  height: 4rem;
  width: 4rem;
}
.brand-text{
  font-weight: 800;
  margin-left: 0.5em;
  font-size: 18pt;
}
/* Styling links */
.flex-links{
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: row;
}
.links{
  width: fit-content;
  list-style: none;
  text-decoration: none;
  margin: 0 1em;
  font-size: 12.5pt;
  color: black;
}
.to-app{
  border-radius: 5px;
  padding: 1em 4em;
  text-decoration: none;
  color: white;
  background-color: /* rgb(18, 18, 170) */ #1649b6
  /* rgb(23, 110, 222)
  rgb(20, 20, 50); */;
  margin-right: 5em;
  font-size: 1.25rem;
}
/* Styling Community drop down */
.community{
  position: absolute;
  bottom: -120px;
  left: 60%;
  height: 120px;
  width: 40px;
  z-index: 1000;
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
