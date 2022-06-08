<template>
  <div>

    <div class="main-wrap">
      <main-header class="main-header" />


      <section id="faq" class="space-top account-bg-color">
        <v-parallax class="parallax-crypto" :src="accountBg">
          <v-container>
            <v-row justify="center" class="mb-12 mt-16 pt-16">
              <v-col md="10" sm="12" cols="12" lg="9">

                <v-row class="d-flex align-center pt-12 justify-center" justify-center align-center>
                  <v-col md="6" sm="10" cols="12" lg="6">
                    <h2 class="text-left">Cryptogate Account Login</h2>
                    <p class="mb-6">Welcome back! Log In with your Email, Phone number or QR code</p>
                    <v-text-field filled label="Username" prepend-inner-icon="person_outline"></v-text-field>
                    <v-text-field v-model="password" filled label="Password" prepend-inner-icon="lock"></v-text-field>
                    <v-btn depressed rounded class="cryptogate-button px-10 font-weight-regular" dark large>
                      Login
                    </v-btn>
                  </v-col>
                  <v-col md="6" sm="10" cols="12" lg="6">
                    <v-img class="align-center justify-center sm-mt-10" contain
                      lazy-src="https://chart.googleapis.com/chart?cht=qr&chl=https%3A%2F%2Fcryptogate-demo.netlify.app%2F&chs=180x180&choe=UTF-8&chld=L|2"
                      max-height="200" max-width="200"
                      src="https://chart.googleapis.com/chart?cht=qr&chl=https%3A%2F%2Fcryptogate-demo.netlify.app%2F&chs=180x180&choe=UTF-8&chld=L|2">
                    </v-img>
                    <h3 class=" mt-6 sm-text-left lg-text-center md-text-center  text-center">Log in with QR code</h3>
                    <p class=" body-2 sm-text-left lg-text-center md-text-center text-center">Scan this code with the Binance mobile app to log in instantly.
                    </p>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
          <Subscribe />
          <main-footer />
        </v-parallax>
      </section>
    </div>
  </div>
</template>

<style lang="scss">
  @import './main';
</style>

<script>
  import HeaderTwo from '~/components/HeaderTwo'
  import Hidden from '~/components/Hidden'
  import Subscribe from '~/components/Subscribe'
  import Footer from '~/components/Footer'
  import PageNav from '~/components/PageNav'
  import Notification from '~/components/Notification'
  import brand from '~/static/text/brand'
  import featureBg from '~/static/images/feature-bg.svg'
  import homeBg from '~/static/images/home-bg.svg'
  import accountBg from '~/static/images/account-bg.svg'

  import SecurityCard from '~/components/Cards/SecurityCard'
  import PageHeadline from '~/components/Cards/PageHeadline'
  export default {
    components: {
      'main-header': HeaderTwo,
      Hidden,
      SecurityCard,
      PageHeadline,
      Subscribe,
      PageNav,
      Notification,
      'main-footer': Footer
    },
    data() {
      return {
        featureBg: featureBg,
        homeBg: homeBg,
        accountBg: accountBg,
        HeadlineData: [{
          title: 'We’re on a mission to accelerate transition to an',
          span: 'open financial system',
          desc: 'Let’s work together! We’ve saved a seat for you.'

        }],
        blogData: [{
            title: 'Frontend Developer',
            more: 'Apply Now',
            desc: 'Associate / Supervisor.'

          },
          {
            title: 'Backend Developer',
            desc: 'Fresh Graduate',
            more: 'Apply Now'
          },
          {
            title: 'UI / UX Designer',
            desc: 'Fresh Graduate / Entry Level',
            more: 'Apply Now'
          },
          {
            title: 'Frontend Developer',
            desc: 'Fresh Graduate',
            more: 'Apply Now'
          },
          {
            title: 'Data Analyst',
            desc: 'Associate / Supervisor.',
            more: 'Are You Ready'
          }
        ]
      }
    },
    head() {
      return {
        title: brand.starter.name + ' - Home Page'
      }
    }
  }
</script>
