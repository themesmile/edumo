<template>
  <div>
    <div class="main-wrap">
      <main-header class="main-header" />
      <main class="container-wrap">
        <section id="home" class="home">
          <v-parallax class="parallax-crypto" :src="homeBg">
            <v-container>
              <animate-slider />
            </v-container>
          </v-parallax>
        </section>

        <section id="comparison" class="comparison">
          <v-container>
            <Comparison />
          </v-container>
        </section>
        <section id="subscribe">
          <Subscribe />
        </section>
      <section id="feature" class="space-top space-bottom">
          <v-parallax  class="parallax-crypto" :src="featureBg">
            <v-container>
              <Feature />
            </v-container>
          </v-parallax>
        </section>
 
           <section id="testimonials" class="space-top">
            <Testimonials />
        </section>
      </main>
      <hidden point="mdDown">
        <page-nav />
      </hidden>
      <hidden point="mdDown">
        <notification />
      </hidden>
      <section id="faq" class="space-top account-bg-color">
        <v-parallax class="parallax-crypto" :src="accountBg">
          <create-account />
          <faq />
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
  import AnimateSlider from '~/components/AnimateSlider'
  import Comparison from '~/components/Comparison'
  import Feature from '~/components/Feature'
  import Counter from '~/components/Counter'
  import Testimonials from '~/components/Testimonials'
  import CreateAccount from '~/components/CreateAccount'
  import Faq from '~/components/Faq'
  import Blog from '~/components/Blog'
  import Subscribe from '~/components/Subscribe'
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
      'animate-slider': AnimateSlider,
      'create-account': CreateAccount,
      Hidden,
      Comparison,
      Feature,
      Counter,
      Testimonials,
      Faq,
      Blog,
      Subscribe,
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
