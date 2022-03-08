<template>
  <div class="timeline">
    <h2 class="section-heading mb">How it works</h2>
    <div class="dot1"></div>
    <div class="dot2"></div>
    <div class="dot3"></div>
    <div class="main-container">
      
      <div class="row justify-center my-2 card">
        
        <div class="text">
          <h3 class="title">Title1</h3>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque.</div>
        <div class="image">Picture</div>
      </div>
      <div class="row justify-center my-2 card">
        <div class="image">Picture</div>
        <div class="text text-right">
          <h3 class="title ">Title2</h3>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque.</div>
      </div>
      <div class="row justify-center my-2 card">
        <div class="text">
          <h3 class="title">Title3</h3>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque.</div>
        <div class="image">Picture</div>
      </div>
    </div>
  </div> 
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class About extends Vue {}

</script>

<style scoped lang="scss">
.timeline{
  position: relative;
  overflow-y: hidden;
}
.row{
  display: flex;
  flex-direction: row;
  overflow-y: hidden;
}
.col{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  overflow-y: hidden;
}
.main-container{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100vw;
  overflow-y: hidden;
}
.justify-center{
  justify-content: center;
  overflow-y: hidden;
}
/* .my-2{
  margin: 2em 0;
} */
.text{
  max-width: 500px;
}
.image{
  width: 300px;
}
/* .line1{
  border: 10px blue solid;
  border-radius: 0 0 0 50px;
  border-top: none;
  border-right: none;
  padding: 2em;
}
.line2{
  border: 10px blue solid;
  border-radius: 0 0 0 50px;
  border-top: none;
  border-left: none;
  padding: 2em;
}
.line3{

} */
.card {
  position: relative;
  max-width: 700px;
  height: 130px;
  overflow-y: hidden;
  margin-bottom: -5px;
}

/* setting padding based on even or odd */
.card:nth-child(odd) {
  padding: 30px 0 30px 30px;
}
.card:nth-child(even) {
  padding: 30px 30px 30px 0;
}
/* Global ::before */
.card::before {
  content: "";
  position: absolute;
  width: 50%;
  border: solid blue;
}

/* Setting the border of top, bottom, left */
.card:nth-child(odd)::before {
  left: 0px;
  top: 0px;
  bottom: 0px;
  border-width: 5px 0 5px 5px;
  border-radius: 50px 0 0 50px;
}

/* Setting the border of top, bottom, right */
.card:nth-child(even)::before {
  right: 0;
  top: 0px;
  bottom: 0;
  border-width: 5px 5px 5px 0;
  border-radius: 0 50px 50px 0;
}

/* Removing the border if it is the first card */
.card:first-child::before {
  border-top: 0;
  border-top-left-radius: 0;
}

/* Removing the border if it is the last card  and it's odd */
.card:last-child:nth-child(odd)::before {
  border-bottom: 0;
  border-bottom-left-radius: 0;
  margin-top: 0px;
}

/* Removing the border if it is the last card  and it's even */
.card:last-child:nth-child(even)::before {
  border-bottom: 0;
  border-bottom-right-radius: 0;
}
.title {
  color: blue;
  position: relative;
}
/* Text-right */
.text-right{
  text-align: right;
}
/* Dots */
.dot1{
  position: absolute;
  width: 10px;
  height: 10px;
  left: calc((100vw - 700px) / 2 - 20px );
  background: white;
  border-radius: 999px;
  border: 3px solid blue;
  z-index: 20;
}
.dot2{
  position: absolute;
  width: 10px;
  height: 10px;
  right: calc((100vw - 700px) / 2 - 35px );
  top: 50%;
  background: white;
  border-radius: 999px;
  border: 3px solid blue;
  z-index: 20;
}
.dot3{
  position: absolute;
  width: 10px;
  height: 10px;
  left: calc((100vw - 700px) / 2 - 20px );
  background: white;
  top: 80%;
  border-radius: 999px;
  border: 3px solid blue;
  z-index: 20;
}

</style>