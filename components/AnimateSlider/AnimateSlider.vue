<template>
  <u-animate-container>
    <div class="hero-cryptogate justify-center pt-16 mt-16">
      <u-animate name="bounceDown" delay="0.5s" duration="0.6s">
        <h1 class="mb-6 text-h4 text-sm-h3 text-md-h2 text-xl-h2 text-lg-h3 font-weight-bold">Crypto App for Everyone</h1>
        <h6 class="mb-8 body-1">Simple. Safe. Hassle-free.Starts from Rp 11.000 </h6>
        <v-btn rounded depressed class="cryptogate-button text-center px-10 font-weight-regular " dark x-large>
          Start Investing Now
        </v-btn>
      </u-animate>
      <v-img class="my-12 rounded-xl" max-width="800" position="center" src="https://via.placeholder.com/727x570?text=Phone+MockUp"></v-img>
    </div>
  </u-animate-container>
</template>

<style lang="scss">
  @import './hero';
</style>
<script>
  import ScrollWrap from '../ScrollWrap'

  export default {
    components: {
      ScrollWrap
    }
  }
</script>
