<template>
  <div class="section">
    <h2 class="section-heading">Roadmap</h2>
<div class="timeline">
  <div class="container left">
    <div class="content">
      <h2>2017</h2>
      <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admodum perfecto mnesarchum, v</p>
    </div>
  </div>
  <div class="container right">
    <div class="content">
      <h2>2016</h2>
      <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admod</p>
    </div>
  </div>
  <div class="container left">
    <div class="content">
      <h2>2015</h2>
      <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admodum perfecto </p>
    </div>
  </div>
  <div class="container right">
    <div class="content">
      <h2>2012</h2>
      <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, ad nec admodum perfecto mnesarchum, </p>
    </div>
  </div>
  <div class="container left">
    <div class="content">
      <h2>2011</h2>
      <p>Lorem ipsum dolor sit amet, quo ei simul congue exerci, </p>
    </div>
  </div>
  
</div>
  </div>
  
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Roadmap extends Vue {}

</script>

<style scoped lang="scss">

* {
  box-sizing: border-box;
}


/* The actual timeline (the vertical ruler) */
.timeline {
  position: relative;
  max-width: 100vw;
  overflow-x: hidden;
  left: 50%;
    -webkit-transform: translateX(-50%) translateY(0);
    -moz-transform: translateX(-50%) translateY(0);
    transform: translateX(-50%) translateY(0);
}

/* The actual timeline (the vertical ruler) */
.timeline::after {
  content: '';
  position: absolute;
  width: 6px;
  background-color: black;
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -3px;
}

/* Container around content */
.container {
  padding: 10px 40px;
  position: relative;
  background-color: inherit;
  width: 40%;
}

/* The circles on the timeline */
/* .container::after {
  content: '';
  position: absolute;
  width: 25px;
  height: 25px;
  right: -17px;
  background-color: blue;
  border: 4px solid #FF9F55;
  top: 50px;
  border-radius: 50%;
  z-index: 1;
} */

/* Place the container to the left */
.left {
  left: 10%;
}

/* Place the container to the right */
.right {
  left: 50%;
}

/* Add arrows to the left container (pointing right) */
.left::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 55px;
  width: 0;
  z-index: 1;
  right: 30px;
  border: medium solid blue;
  border-width: 1px 0 3px 30px;
  /* border-color: transparent transparent transparent blue; */
}

/* Add arrows to the right container (pointing left) */
.right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 55px;
  width: 0;
  z-index: 1;
  left: 30px;
  border: medium solid blue;
  border-width: 1px 0 3px 30px;
  /* border-color: transparent blue transparent transparent; */
}

/* Fix the circle for containers on the right side */
.right::after {
  left: -16px;
}
/* Fix the circle for containers on the left side */
.left::after {
  left: 98.9%;
}

/* The actual content */
.content {
  padding: 20px 60px;
  background-color: transparent;
  position: relative;
  border-radius: 6px;
}

/* Media queries - Responsive timeline on screens less than 600px wide */
@media screen and (max-width: 600px) {
  /* Place the timelime to the left */
  .timeline::after {
  left: 31px;
  }
  
  /* Full-width containers */
  .container {
  width: 100%;
  padding-left: 70px;
  padding-right: 25px;
  }
  
  /* Make sure that all arrows are pointing leftwards */
  .container::before {
  left: 60px;
  border: medium solid blue;
  border-width: 10px 10px 10px 0;
  border-color: transparent blue transparent transparent;
  }

  /* Make sure all circles are at the same spot */
  .left::after, .right::after {
  left: 15px;
  }
  
  /* Make all right containers behave like the left ones */
  .right {
  left: 0%;
  }
}


</style>