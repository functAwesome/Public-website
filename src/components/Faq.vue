<template>
  <div class="section my-margin">
    <div class="wrapper">
        <h2 class="section-heading ">FAQ</h2>
            <div class="container">
      <details class="faq-card">
        <summary>How do I pay for the Essentials or Premium plan? <span class="faq-open-icon">+</span></summary>
        <span class="faq-card-spoiler">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ornare, sem at dictum faucibus, neque nunc pellentesque sem, nec pellentesque tellus ex vel lorem. Vestibulum magna odio, ornare in faucibus.</span>
      </details>
      <details class="faq-card">
        <summary>Can I cancel my Essentials or Premium plan subscription at any time? <span class="faq-open-icon">+</span></summary>
        <span class="faq-card-spoiler">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ornare, sem at dictum faucibus, neque nunc pellentesque sem, nec pellentesque tellus ex vel lorem. Vestibulum magna odio, ornare in faucibus.</span>
      </details>
      <details class="faq-card">
        <summary>We need to add new users to our team. How will that be billed? <span class="faq-open-icon">+</span></summary>
        <span class="faq-card-spoiler">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ornare, sem at dictum faucibus, neque nunc pellentesque sem, nec pellentesque tellus ex vel lorem. Vestibulum magna odio, ornare in faucibus.</span>
      </details>
      <details class="faq-card">
        <summary>My team wants to cancel its subscription. How do we do that? Can we get a refund? <span class="faq-open-icon">+</span></summary>
        <span class="faq-card-spoiler">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ornare, sem at dictum faucibus, neque nunc pellentesque sem, nec pellentesque tellus ex vel lorem. Vestibulum magna odio, ornare in faucibus.</span>
      </details>
      <details class="faq-card">
        <summary>Do you offer discounts for non-profit organizations or educational institutions? <span class="faq-open-icon">+</span></summary>
        <span class="faq-card-spoiler">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer ornare, sem at dictum faucibus, neque nunc pellentesque sem, nec pellentesque tellus ex vel lorem. Vestibulum magna odio, ornare in faucibus.</span>
      </details>
    </div>
    </div>
</div>  
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Faq extends Vue {}

</script>

<style scoped lang="scss">
.container {
  max-width: 970px;
  margin: 0 auto;
}

.faq-heading {
  margin-top: 45px;
  margin-bottom: 15px;
  text-align: center;
  font-weight: 400;
  font-size: 30px;
}

.faq-card {
  border: 1px solid #dce0e8;
  border-radius: 6px;
  padding: 24px 20px;
  margin-bottom: 12px;
  list-style: none;
  position: relative;
  cursor: pointer;
}

.faq-open-icon {
  font-size: 22px;
  position: absolute;
  top: 18px;
  right: 24px;
  font-weight: 700;
}

details[open] .faq-open-icon {
  top: 18px;
  right: 24px;
}

details > summary {
  list-style: none;
}

details > summary::-webkit-details-marker {
  display: none;
}

details[open] summary {
  color: #000;
  font-weight: 500;
}

details[open] .faq-card-spoiler {
  display: inline-block;
  padding-top: 8px;
  color: #8b8b9a;
}

.faq-aftertext {
  text-align: center;
  color: #8b8b9a;
}
</style>