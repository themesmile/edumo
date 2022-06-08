<template>

  <div class="feature-more">
    <v-container>
      <v-row class="mt-16">
        <v-col cols="12" sm="12" class="mt-16 text-center">
          <h2 class="font-weight-medium display-2 font-weight-bold mb-3">Easy, even for beginners.</h2>
          <p class="body-1">Experience a different investing experience. <br>Trade, analyze, manage assets, and learn
            about crypto.
            Find all your investment needs on Crypto.</p>
        </v-col>
      </v-row>
      <v-row justify="space-around">

        <v-btn depressed dark large rounded class="comparison-button text-capitalize">
          Start Investing Now
          <v-icon class="ml-4">arrow_forward</v-icon>
        </v-btn>
      </v-row>

      <u-animate-container>
        <v-row justify="center d-flex align-center">
          <v-col md="6" class="px-6" cols="12">
            <div class="feature-item">
              <u-animate name="fadeInLeft" delay="0.5s" duration="0.6s">
                <kinesis-container>
                  <kinesis-element :strength="20" type="depth">
                    <figure class="img">
                      <v-img class="my-12 feature-image" position="center" :src="featureImage01" contain
                        max-height="450"></v-img>
                    </figure>
                  </kinesis-element>
                </kinesis-container>


              </u-animate>
            </div>
          </v-col>
          <v-col md="6" class="px-6" cols="12">
            <div class="feature-item">
              <u-animate name="fadeInLeft" duration="0.6s">
                <h5 class="title-app display-5 mb-3">Step <span class="font-weight-bold">.01</span></h5>
              </u-animate>
              <u-animate name="fadeInLeft" duration="0.6s">
                <h1 class="title font-weight-bold mb-3">Sign Up and Verify in 10 minutes</h1>
              </u-animate>
              <u-animate name="fadeInRight" delay="0.5s" duration="0.6s">
                <p class="text body-1">
                  Sign up with your email, verify your account by taking a photo of your KTP, SIM, or passport.
                </p>
              </u-animate>
            </div>
          </v-col>
        </v-row>
      </u-animate-container>



      <u-animate-container>
        <v-row justify="center d-flex align-center flex-row-reverse">
          <v-col md="6" class="px-1" cols="12">
            <div class="feature-item">
              <u-animate name="fadeInLeft" delay="0.5s" duration="0.6s">
               <kinesis-container>
                  <kinesis-element :strength="20" type="depth">
                    <figure class="img">
                      <v-img class="my-12 feature-image" position="center" :src="featureImage01" contain
                        max-height="450"></v-img>
                    </figure>
                  </kinesis-element>
                </kinesis-container>

              </u-animate>
            </div>
          </v-col>
          <v-col md="6" class="px-6" cols="12">
            <div class="feature-item">
              <u-animate name="fadeInLeft" duration="0.6s">
                <h5 class="title-app display-5 mb-3">Step <span class="font-weight-bold">.02</span></h5>
              </u-animate>
              <u-animate name="fadeInLeft" duration="0.6s">
                <h1 class="title font-weight-bold mb-3">FREE Deposit</h1>
              </u-animate>
              <u-animate name="fadeInRight" delay="0.5s" duration="0.6s">
                <p class="text body-1">
                  Deposit your Rupiah balance by transferring funds from banks or your preferred e-wallets.
                </p>
              </u-animate>
            </div>
          </v-col>
        </v-row>
      </u-animate-container>

      <u-animate-container>
        <v-row justify="center d-flex align-center">
          <v-col md="6" class="px-6" cols="12">
            <div class="feature-item">
              <u-animate name="fadeInLeft" delay="0.5s" duration="0.6s">
                     <kinesis-container>
                  <kinesis-element :strength="20" type="depth_inv">
                    <figure class="img">
                      <v-img class="my-12 feature-image" position="center" :src="featureImage01" contain
                        max-height="450"></v-img>
                    </figure>
                  </kinesis-element>
                </kinesis-container>
              </u-animate>
            </div>
          </v-col>
          <v-col md="6" class="px-6" cols="12">
            <div class="feature-item">
              <u-animate name="fadeInLeft" duration="0.6s">
                <h5 class="title-app display-5 mb-3">Step <span class="font-weight-bold">.03</span></h5>
              </u-animate>
              <u-animate name="fadeInLeft" duration="0.6s">
                <h1 class="title font-weight-bold mb-3">Start Investing, No Additional Fees</h1>
              </u-animate>
              <u-animate name="fadeInRight" delay="0.5s" duration="0.6s">
                <p class="text body-1">
                  Experience the easiest way to buy and sell crypto assets.
                </p>
              </u-animate>
            </div>
          </v-col>
        </v-row>
      </u-animate-container>


    </v-container>
  </div>
</template>

<style lang="scss">
  @import './feature-styles';
</style>

<script>
  import ScrollWrap from '../ScrollWrap'
  import imgAPI from '~/static/images/imgAPI'
  import featureImage01 from '~/static/images/login.png'

  export default {
    components: {
      ScrollWrap
    },
    data() {
      return {
        imgAPI,
        featureImage01: featureImage01
      }
    }
  }
</script>
