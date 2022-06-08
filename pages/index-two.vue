<template>
  <div>
    <div class="main-wrap">
      <main-header class="main-header" />
      <main class="container-wrap">
        <section id="home" class="home">
          <v-parallax class="parallax-crypto" :src="homeBg">
            <v-container>
              <animate-slider-two />
            </v-container>
          </v-parallax>
        </section>
        <section id="comparison" class="comparison">
          <ComparisonTwo />
        </section>
        <section id="feature" class="space-top space-bottom">
          <v-parallax class="cryptogate-parallax" :src="featureBg">
            <v-container>
              <FeatureTwo />
            </v-container>
          </v-parallax>
        </section>
        <section id="testimonials" class="space-top">
          <v-container>
            <TestimonialsTwo />
          </v-container>
        </section>
      </main>
      <hidden point="mdDown">
        <page-nav />
      </hidden>
      <!-- <hidden point="mdDown">
        <notification />
      </hidden> -->
      <section id="faq" class="space-top account-bg-color">
        <v-parallax class="parallax-crypto" :src="accountBg">
          <SubscribeTwo />
           <FaqTwo />
          <Blog />
         
          <create-account />
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
  import Header from '~/components/Header'
  import Hidden from '~/components/Hidden'
  import AnimateSliderTwo from '~/components/AnimateSliderTwo'
  import ComparisonTwo from '~/components/ComparisonTwo'
  import FeatureTwo from '~/components/FeatureTwo'
   import CreateAccount from '~/components/CreateAccount'
  import Counter from '~/components/Counter'
  import TestimonialsTwo from '~/components/TestimonialsTwo'
  import FaqTwo from '~/components/FaqTwo'
  import Blog from '~/components/Blog'
  import SubscribeTwo from '~/components/SubscribeTwo'
  import Footer from '~/components/Footer'
  import PageNav from '~/components/PageNav'
  import Notification from '~/components/Notification'
  import brand from '~/static/text/brand'
  import featureBg from '~/static/images/feature-bg.svg'
  import homeBg from '~/static/images/home-bg.svg'
  import accountBg from '~/static/images/account-bg.svg'


  export default {
    components: {
      'main-header': Header,
      'animate-slider-two': AnimateSliderTwo,
      'create-account': CreateAccount,
      Hidden,
      ComparisonTwo,
      FeatureTwo,
      Counter,
      TestimonialsTwo,
      FaqTwo,
      Blog,
      SubscribeTwo,
      PageNav,
      Notification,
      'main-footer': Footer
    },
    data() {
      return {
        featureBg: featureBg,
        homeBg: homeBg,
        accountBg: accountBg
      }
    },
    head() {
      return {
        title: brand.starter.name + ' - Home Page'
      }
    }
  }
</script>
