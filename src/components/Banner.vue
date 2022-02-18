<template>
  <div class="section">
      <div class="banner">
      <div class="text-box">
          <h1 class="uppercase">Massive text of something</h1>
          <h2>Smaller Text</h2>
      </div>
      <img src="" alt="">
      <div class="analytics-area">
          <div class="analytics-box">
              <div class="data-div">Data1</div> <div class="vl" />
              <div class="data-div">Data2</div> <div class="vl" />
              <div class="data-div">Data3</div>
          </div>
      </div>
  </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Navbar extends Vue {
  topOfPage = true;
  name = 'hello';
  handleScroll(){
      if(window.pageYOffset>0){
        if(this.topOfPage) this.topOfPage = false
      } else {
        if(!this.topOfPage) this.topOfPage = true
      }
    }
  test = (): void => {
    this.name = 'Hello Wrold!';
    console.log('this is test and called');
  };
  beforeMount = (): void => {
    this.test();
    window.addEventListener('scroll', this.handleScroll)
  }
}
  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Hahmlet&display=swap');
.banner {
    width: 90%;
    height: 90vh;
    background-color: white;
    z-index: -3;
    overflow-x: hidden;
    margin: 0;
}
.text-box{
    position: absolute;
        width: 40vw;
        height:auto;
        margin-left: 7em;
        margin-top: 32vh;
    }
    .uppercase{
        text-transform: uppercase;
    }
h1 {
    font-size: 40pt;
    font-family: 'Hahmlet', serif;
    text-align: center;
}
h2 {
    font-size: 20pt;
    font-family: 'Hahmlet', serif;
    text-align: center;
}
.data-div{
    z-index: 20;
}
.analytics-area{
    position: absolute;
    width: 90vw;
    height: 150px;
    bottom: 0px;
}
.analytics-box{
    position: static;
    width: 60vw;
    height: 100px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    margin-left: auto;
    margin-right: auto;
    z-index: 3;
}

.vl {
  border-left: 6px solid rgb(23, 110, 222);
  height: 50px;
}
</style>
