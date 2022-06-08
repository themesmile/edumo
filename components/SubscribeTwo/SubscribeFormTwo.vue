<template>
  <v-container class="my-16">
    <h6 class="text-center subtitle-2 font-weight-medium mt-16 mb-6">Given the enormous wealth creation from
      cryptocurrency</h6>
 


    <div class="subscribe-wrap pa-12 rounded-xl ">
      <v-row justify="center d-flex align-center">
        <v-col xl="4" lg="4" md="12" sm="12"  class="px-3 ">
          <h3 class="text-left md-text-center white--text display-1 font-weight-medium">Stay up to date with the latest insights</h3>
        </v-col>
        <v-col xl="1" lg="1" md="12" sm="12" class="d-none d-md-flex d-lg-flex">
          <v-divider style="height:200px" vertical light insight white></v-divider>
        </v-col>

        <v-col xl="7" lg="7" md="12" sm="12"  class="px-3">
          <h6 class="text-left white--text headline font-weight-medium mb-3">Enter your email address to unlock the world of Centili updates and content</h6>

          <v-text-field background-color="rgba(255,255,255,0.9)" color="#ffffff" placeholder="Your email address"
            class="pr-0 cryptogate-input mb-0" filled rounded light v-model="input" @keypress.enter="show">

            <template v-slot:append class="pt-0">

              <v-btn depressed rounded color="#FF5934" large class="px-15 mt-n3 ml-n1 cryptogate-subcribe white--text d-none d-md-flex d-lg-flex"
                @click="show">

                Submit

              </v-btn>

            </template>

          </v-text-field>

          <h6 class="white--text caption font-weight-reguler"> By submitting your email you acknowledge that you have read and understood our Privacy Policy. </h6>
        </v-col>
      </v-row>
    </div>

  </v-container>
</template>

<style lang="scss">
  @import './subscribe-style';
</style>
<script>
  import imgAPI from '~/static/images/imgAPI'
  export default {
    data() {
      return {
        message1: 'yourname@hosting.com',
        partner01: imgAPI.partners[1],
        partner02: imgAPI.partners[2],
        partner03: imgAPI.partners[3],
        partner04: imgAPI.partners[4],
        partner05: imgAPI.partners[5],
        partner06: imgAPI.partners[6],
      }
    }
  }
</script>
