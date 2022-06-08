<template>
  <v-container tag="footer" class="footer mt-16 pt-8">
    <v-row>
      <v-col md="4" cols="12">
        <div class="logo">
          <img :src="logo" alt="logo">
          <h6 class="mb-2 mt-2 body-1 text-left font-weight-bold">
            {{ brand.starter.projectName }}
          </h6>
        </div>
        <p class="body-2 pr-10">Assets stored on Pintu are protected and secured by curv.co technology. fingerprint
          scanner, face ID.</p>
      </v-col>
      <v-col class="pa-4" md="8" cols="12">
        <v-expansion-panels v-if="isMobile">
          <v-expansion-panel v-for="(footer, index) in footers" :key="index" class="accordion-content">
            <v-expansion-panel-header>
              <h6 class="body-1 mb-4">
                {{ footer.title }}
              </h6>
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <ul>
                <li v-for="(item, index) in footer.description" :key="index">
                  <nuxt-link :to="footer.link[index]">
                    {{ item }}
                  </nuxt-link>
                </li>
              </ul>

            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
        <v-row v-if="isDesktop" justify="space-around">
          <v-col v-for="(footer, index) in footers" :key="index" class="pa-4 site-map-item">
            <h6 class="body-1 font-weight-bold mb-4">
              {{ footer.title }}
            </h6>
            <ul>
              <li class="body-2 mb-4" v-for="(item, index) in footer.description" :key="index">

                <nuxt-link :to="footer.link[index]">
                 {{ item }}
                </nuxt-link>
              </li>

            </ul>


          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row>
      <v-col md="12" cols="12">
        <p class="caption mb-6">Trading and investing in crypto assets is a high-risk activity. Past information does
          not reflect future performance. Historical performance, expected returns, and projected probabilities are
          provided for informational and illustration purposes. All decisions on trading crypto assets are independent
          decisions by the user.
        </p>
      </v-col>
    </v-row>
    <v-divider class="mb-4"></v-divider>
    <v-row>
      <v-col lg="12" md="12" cols="12">
        <p class="text-center caption">
          &copy;&nbsp; {{ brand.starter.footerText }} </p>
      </v-col>
    </v-row>

  </v-container>
</template>

<style lang="scss">
  @import './footer-style';
</style>

<script>
  import logo from '~/static/images/cryptogate-icon.svg'
  import brand from '~/static/text/brand'

  export default {
    data: () => ({
      logo: logo,
      brand: brand,
      lang: 'en',
      footers: [{
          title: 'Company',
          description: ['Team', 'History', 'Contact us', 'Locations'],
          link: ['#team', '#history', '#contact-us', '#locations']
        },
        {
          title: 'Products',
          description: [
            'Resource',
            'Resource name',
            'Another resource',
            'Final resource'
          ],
          link: [
            '#resource',
            '#resource-name',
            '#another-resource',
            '#final-resource'
          ]
        },
        {
          title: 'Social Media',
          description: ['Facebook', 'Twitter', 'Google'],
          link: ['#privacy-policy', 'https://twitter.com/themesmile', '#terms-of-use']
        },
        {
          title: 'Our Office',
          icon: 'meeting_room',
          description: ['3517 W. Gray St. Utica, Pennsylvania 57867'],
          link: ['#privacy-policy', '#terms-of-use']
        }

      ]
    }),
    mounted() {
      this.lang = this.$i18n.locale
    },
    computed: {
      langList: function () {
        const list = []
        this.$i18n.locales.map(item => {
          list.push({
            text: this.$t('common.' + item.code),
            value: item.code
          })
        })
        return list
      },
      isMobile() {
        const smDown = this.$store.state.breakpoints.smDown
        return smDown.indexOf(this.$mq) > -1
      },
      isDesktop() {
        const mdUp = this.$store.state.breakpoints.mdUp
        return mdUp.indexOf(this.$mq) > -1
      }
    },
    methods: {
      switchLang: function (val) {
        this.$i18n.setLocale(val)
      }
    }
  }
</script>
