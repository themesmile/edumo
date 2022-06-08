<template>
  <div>
    <div class="main-wrap">
      <main-header class="main-header" />
      <main class="container-wrap">
        <section id="security" class="security">
          <v-parallax class="parallax-crypto" :src="homeBg">
            <BlogPage />
          </v-parallax>
        </section>
      </main>
      <section id="faq" class="space-top account-bg-color">
        <v-parallax class="parallax-crypto" :src="accountBg">
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
  import BlogPage from '~/components/BlogPage'
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
      BlogPage,
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
          title: 'Lastest News',
          span: '',
          desc: 'All the latest news and updates about Phantom the product, the company, and the team'

        }],
        blogData: [{
            title: 'We never have access to your funds or private keys',
            desc: 'Crtyptogate is a self-custodial wallet. Your private keys are encrypted on your device by your password and are never shared with anyone.',
            more: 'Learn More'
          },
          {
            title: 'Independently audited',
            desc: 'Our code has been audited by Kudelski Security, a top software auditing firm trusted by technology companies worldwide.',
            more: 'Read the Report'
          },
          {
            title: 'Your privacy is respected',
            desc: 'Phantom wallet doesn’t track any personal identifiable information, your account addresses or asset balances.',
            more: 'Go to Privacy Policy'
          },
          {
            title: 'Check out our bug bounty',
            desc: 'White hat hackers can be rewarded up to $50,000 for finding vulnerabilities that may result in the loss of user funds.',
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
