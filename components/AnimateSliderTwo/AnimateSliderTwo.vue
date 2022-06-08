<template>

  <div class="hero-cryptogate-two">
    <v-row no-gutters class="d-flex align-center">
      <v-col cols="12" lg="7" md="7" sm="12">
        <!-- <vue-typed-js :strings="['Begginer', 'Trader','Everyone']" :loop="true" :cursorChar="'|'" :fadeOutDelay="1000"
          :typeSpeed="300">
          <h3 class="mb-6 text-h4 text-sm-h6 text-md-h2 text-xl-h5 font-weight-bold ">Crypto App foryou <br><span
              class="text-md-h2 text-xl-h1 typing font-weight-bold"></span></h3>
        </vue-typed-js> -->
         <h3 class="mb-6 text-h4 text-sm-h6 text-md-h2 text-xl-h5 font-weight-bold ">Online learning through <br><span
              class="text-md-h2 text-xl-h1 typing font-weight-bold">SaaS technology</span></h3>
        <h6 class="mb-8 body-1">We have ready-to-used learning contents for your business.Soft and hard skill in various field, Small and medium enterprises (UMKM) learning and more


</h6>
        <v-btn rounded depressed dark x-large class="cryptogate-button px-10 font-weight-regular">
           <v-icon left medium light >
           play_circle
          </v-icon>
          request demo
        </v-btn>
        <v-btn depressed x-large class="cryptogate-button-secondary px-10 ml-2 font-weight-regular rounded-lg">
          Explore more
          <v-icon right>
            east
          </v-icon>
        </v-btn>
      </v-col>
      <v-col cols="12" lg="5" md="5" sm="12">
        <v-img class="my-12" max-width="600" position="center" :src="ilustration"></v-img>
      </v-col>
    </v-row>
  </div>

</template>

<style lang="scss">
  @import './hero-two';
</style>
<script>
  import ScrollWrap from '../ScrollWrap'
  import ilustration from '~/static/images/edumo-main.png'
  export default {
    components: {
      ScrollWrap

    },
    data() {
      return {
        ilustration: ilustration
      }
    }
  }
</script>
