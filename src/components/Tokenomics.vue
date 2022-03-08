<template>
  <div class="section my-margin">
      <h2 class="section-heading mb">Tokenomics</h2>
      <div class="col px-10">
          <div class="graph"></div>
          <div>
              <h3>Sample text</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque.</p>
          </div>
      </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';


@Component
export default class Tokenomics extends Vue {
  
}
  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.row{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
}
.col{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.graph{
    width: 700px;
    height: 500px;
    background-image: url('../assets/graph.png');
    background-size: contain;
    background-repeat: no-repeat;
}
.px-10{
    padding: 0 20rem;
}
</style>
