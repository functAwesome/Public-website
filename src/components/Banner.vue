<template>
  <div class="section mb-7">
      <div class="banner">
      <div class="text-box">
        
          <h1 class="uppercase">SET &amp; FORGET <br> CRYPTO LOANS</h1>
          <h2>The first community backed lending protocol powered by the Cardano Blockchain </h2>
          <a class="to-app" href="https://app.yamfore.com">LAUNCH</a>
      </div>
      <img src="" alt="">
      <!-- <div class="analytics-area">
          <div class="analytics-box">
              <div class="data-div"><div class="my-5">20%</div><div><b>Collateral Requirement</b></div></div> 
              <div class="data-div"><div class="my-5">10M+</div><div><b>Yam Marketcap</b></div></div> 
              <div class="data-div"><div class="my-5">1000</div><b>Active loans</b><div></div></div>
          </div>
      </div> -->
  </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';


@Component
export default class Banner extends Vue {
  topOfPage = true;
  name = 'hello';
  
  handleScroll(){
      if(window.pageYOffset>0){
        if(this.topOfPage) this.topOfPage = false
      } else {
        if(!this.topOfPage) this.topOfPage = true
      }
    }
  beforeMount = (): void => {
    window.addEventListener('scroll', this.handleScroll)
  }
  
}
  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Hahmlet&display=swap');
.banner {
    width: 100%;
    height: 70vh;
    background-color: white;
    z-index: -3;
    
    
    overflow-x: hidden;
    margin: 0;
}
.mb-7{
  margin-bottom: 7em;
}
.text-box{
    position: absolute;
    padding: 1em;
    padding-bottom: 7em;
        width: 40vw;
        height:fit-content;
        
        margin-left: 7em;
        margin-top: 30vh;
        display: flex;
        flex-direction: column;
    }
    .uppercase{
        text-transform: uppercase;
        font-size: 56px;
    }
/* To app styling */
.to-app{
  position: absolute;
  text-decoration: none;
  color: white;
  background-color: /* rgb(18, 18, 170) */ #1649b6
  /* rgb(23, 110, 222)
  rgb(20, 20, 50); */;
  border-radius: 5px;
  padding: 1em 4em;
  bottom: 0;
  left: 1em;
  text-align: center;
  font-size: 1.25rem;
  font-weight: 900;
}
/* styling banner img */
.banner-img{
  position: absolute;
  bottom: 100px;
  right: 6vw;
  width: 30vw;
  z-index: 1;
}
h1 {
    font-size: 56px;
    font-family: Arial, Helvetica, sans-serif;
    text-align: left;
    font-weight: 900;
}
h2 {
    font-size: 24px;
    font-family: Arial, Helvetica, sans-serif;
    text-align: left;
    font-weight: 300;
}
.data-div{
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 0px 8px 20px 7px rgba(0,0,0,0.27);
    -webkit-box-shadow: 0px 8px 20px 7px rgba(0,0,0,0.27);
    -moz-box-shadow: 0px 8px 20px 7px rgba(0,0,0,0.27);
    margin: 5em 0;
  padding: 1.9em;
    z-index: 20;
  width: 200px;
}
.my-5{
  margin: 5px 0;
  font-size: 40pt;
}

.analytics-area{
    position: absolute;
    width: 100vw;
    height: 200px;
    bottom: 10px;
    display: flex;
    align-items: center;
    z-index: 2;
}
.analytics-box{
    position: static;
    width: 60vw;
    height: fit-content;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    margin-left: auto;
    margin-right: auto;
    z-index: 3;
    background-color: white;
    border-radius: 20px;
    
}

.vl {
  border-left: 6px solid rgb(23, 110, 222);
  height: 50px;
}
</style>
