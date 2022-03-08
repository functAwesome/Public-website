<template>

        <div class="ellipses-container" v-bind:class="position">

            <div class="ellipses ellipses__outer--thin" >

                <div class="ellipses ellipses__orbit"></div>

            </div>

            <div class="ellipses ellipses__outer--thick"></div>
        </div>  
  
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
@Component
export default class Orbiter extends Vue {
    @Prop({ default: 'one' })
    position!: string
}

</script>

<style scoped lang="scss">
$tiber: #09383E;
$elephant: #0C383E;
$white: #fff;

// rem font sizing.

.ellipses-container {
    width: 50rem;
    height: 50rem;
    display: block;
    border-radius: 50%;
    margin: 0;
    position: absolute;
    padding:20em;
    z-index: 50;
}
.one{
    top: 1.5rem;
    left:-25rem;
}
.two{
top: 1.5rem;
  right:-25rem;
}
.three{
top: 1.5rem;
  left:-25rem;
}
.four{
top: 1.5rem;
  left:-25rem;
}

.ellipses {
    border-radius: 50%;
    position: absolute;
    top: 0;
    border-style: solid;
}

.ellipses__outer--thin {
    width: 50%;
    height: 50%;
    border-width: 1px;
    border-color: rgba(9, 56, 62, 0.1);
    animation: ellipsesOrbit 15s ease-in-out infinite;


    &:after {
      content: "";
      background-image: url('https://s29.postimg.org/5h0r4ftkn/ellipses_dial.png');
      background-repeat: no-repeat;
      background-position: center;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      position: absolute;
      opacity: 0.15;
    }
}

.ellipses__outer--thick {
    width: 49.5%;
    height: 49.5%;
    border-color: $tiber transparent;
    border-width: 2px;
    transform: rotate(-45deg);
    animation: ellipsesRotate 15s ease-in-out infinite;
}

.ellipses__orbit {
    width: 2.5rem;
    height: 2.5rem;
    border-width: 2px;
    border-color: $tiber;
    top: 5rem;
    right: 6.75rem;

    &:before {
        content: '';
        width: 0.7rem;
        height: 0.7rem;
        border-radius: 50%;
        display: inline-block;
        background-color: $tiber;
        margin: 0 auto;
        left: 0;
        right: 0;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);

    }
}


@keyframes ellipsesRotate {
    0% {
        transform: rotate(-45deg);
    }

    100% {
        transform: rotate(-405deg);
    }
}

@keyframes ellipsesOrbit {
    0% {
        transform: rotate(0);
    }

    100% {
        transform: rotate(360deg);
    }
}
</style>