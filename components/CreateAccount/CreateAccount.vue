<template>
  <v-container class="mb-16">

    <h3 class="display-2 font-weight-bold text-center mb-6 mt-16 pt-16 ">
      Create an Account Now
    </h3>
    <p class="body-1 text-center mb-6">
      Sign up in a matter of minutes, start investing<br> right away
    </p>
    <v-row justify="center">
      <v-col lg="2" md="2">
        <v-img max-height="60" contain :src="AppStore"></v-img>
      </v-col>
      <v-col lg="2" md="2">
        <v-img max-height="60" contain :src="GoogleStore"></v-img>
      </v-col>
    </v-row>


    <div class="subscribe-wrap  rounded-xl mt-16">
      <v-parallax class="parallax-crypto pa-15" height="200" :src="accountBg">
        <v-row justify="center d-flex align-center">
          <v-col xl="12" lg="12" md="12" sm="12" class="px-6 ">
            <h5 class="text-center white--text headline font-weight-medium">Invite your friend to invest in Cryptogate.
              <br>
              Get up to $ 10 for their first purchase.</h5>
          </v-col>
        </v-row>
      </v-parallax>
    </div>

  </v-container>
</template>

<style lang="scss">
  @import './create-account-style';
</style>

<script>
  import accountBg from '~/static/images/cta-bg.svg'
  import GoogleStore from '~/static/images/google-playstore.svg'
  import AppStore from '~/static/images/app-store.svg'
  export default {

    data() {
      return {
        accountBg: accountBg,
        GoogleStore: GoogleStore,
        AppStore: AppStore
      }
    }
  }
</script>
