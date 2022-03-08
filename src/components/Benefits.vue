<template>
  <div class="section my-margin">
    <div class="wrapper">
        <div class='row'>
            <div class='column'>
                <div class='box shadow'>
                    <img src="" alt="">
                   <h3>No Interest payments</h3>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque.
                </div>
            </div>
            <div class='column'>
                <div class='box shadow'>
                    <img src="" alt="">
                   <h3>No Margin Calls</h3>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque.
                </div>
            </div>
            <div class='column'>
                <div class='box shadow'>
                    <img src="" alt="">
                    <h3>Up to three year loan terms</h3>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Commodo sed egestas egestas fringilla phasellus faucibus scelerisque.
                </div>
            </div>
        </div>
    </div>
</div>  
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Benefits extends Vue {}

</script>

<style scoped lang="scss">
.wrapper{
    padding: 2em 5em;
}
.row{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}
.column{
    display: flex;
    flex-direction: column;
    margin: 0 1em;
    
}
h3{
    margin-bottom: 2em;
}
.box{
    position: relative;
    background-color: white;
    margin: 40px;
    text-align: center;
  padding: 15px;
  width: 200px;
    height: 300px;
    padding: 1em;
}
.shadow{
    box-shadow: 0px 8px 20px 7px rgba(0,0,0,0.27);
    -webkit-box-shadow: 0px 8px 20px 7px rgba(0,0,0,0.27);
    -moz-box-shadow: 0px 8px 20px 7px rgba(0,0,0,0.27);
}
.text-white{
    color: white;
}
</style>