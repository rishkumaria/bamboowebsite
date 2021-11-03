<template>
  <section id="contact" class="light-section">
    <div class="container-fluid">
      <h1 class="section-header">{{ heading }}</h1>
      <div class="row">
        <div
          class=""
          style="margin: 0 auto;"
        >
          <div class="contact-content">
            <h2>Out of our 17.77bn token supply, 19.5% of has been paid to the dev team.</h2>
            <h2>20% of the supply was staked into the liquidity pool.</h2>
            <h2>The remaining 60.5% of the tokens were airdropped to a community of PandaStreet and Cheems NFT holders.</h2>
            <h2>Our team believes in the community we create and we take pride in the trust the community has given us back.</h2>



          </div>
        </div>
      </div>
    </div>

    <div class="row arrow-container">
      <a class="arrow-icon" href="#">
        <i class="fas fa-chevron-up fa-4x"></i>
      </a>
    </div>

  </section>
</template>

<script>
import data from "../../data/data.json";

export default {
  name: "Contact",
  props: {},
  components: {},
  data() {
    return {
      contact: data.contact,
      social: data.contact.social,
      heading: data.main.headings.contact,
    };
  },
};
</script>

<style lang="scss"></style>
