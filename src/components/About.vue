<template>
  <div class="section">
    <h2 class="section-heading">How it works</h2>
    <div class="wrapper">
        <div class='row'>
    <div class='column'>
      <div class='box-height block1'>
        Some Text in Column One
        <hr>
      </div>
    </div>
    <div class='column'>
      <div class='box-height block2'>
        Some Text in Column Two
      </div>
    </div>
    
  </div>
  <div class='row'>
    <div class='column'>
      <div class='box-height block3'>
        Some Text in Row 2, Column One
      </div>
    </div>
    <div class='column'>
      <div class='box-height block4'>
        Some Text in Row 2, Column Two
      </div>
    </div>
</div>
<div class='row'>
    <div class='column'>
      <div class='box-height block5'>
        Some Text in Row 2, Column One
      </div>
    </div>
    <div class='column'>
      <div class='box-height block6 bordered'>
        Some Text in Row 2, Column Two
      </div>
    </div>
</div>
    </div>
  
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque. Massa tincidunt nunc pulvinar sapien et ligula. Tortor condimentum lacinia quis vel eros donec ac odio.</p>
</div>  
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class About extends Vue {}

</script>

<style scoped lang="scss">

.wrapper{
    padding: 0 3rem;
}
.row {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  width: 100%;
}

.column {
  display: flex;
  flex-direction: column;
  flex-basis: 100%;
  flex: 1;
}
.box-height{
    height: 30vh;
}

.block1{
    border-left: 4px dashed black;
}
.block2{
    
}
.block3{
border-top: 4px dashed black;
border-right: 4px dashed black;
border-bottom: 4px dashed black;
}
.block4{

}
.block5{

}
.block6{

}
.bordered {
  display: inline-block;
  padding: 20px;
  border: dashed 4px #000;
  
  border-image: url("http://i.stack.imgur.com/wLdVc.png") 2 round;
}


/*The border image of this one creates wider gaps*/
.largeGaps {
  border-image-source: url("http://i.stack.imgur.com/LKclP.png");
  margin: 0 20px;
}
</style>