<template>
  <div>

    <div class="main-wrap">
      <main-header class="main-header" />
      <main class="container-wrap">


        <section class="main-top-bg">
          <v-parallax class="parallax-crypto" :src="homeBg">
            <v-container>
              <v-row justify="center" class="mb-12">
                <v-col md="8" cols="8" lg="8" class="justify-center">
                  <div v-for="(item, index) in HeadlineData" :key="index">
                    <page-headline :title="item.title" :span="item.span" :desc="item.desc" />
                  </div>

                </v-col>
              </v-row>
              <h4 class="text-left font-weight-bold ">Crypto Price Today</h4>
              <v-simple-table  class="mt-6 rounded-xl">
                <template :elevation="n - 6" v-slot:default>
                  <thead>
                    <tr>
                      <th class="text-left px-10 py-5 body-2 font-weight-bold text-uppercase">
                        Name
                      </th>
                      <th class="text-left px-5 py-5 body-2 font-weight-bold text-uppercase text-left">
                        Price
                      </th>
              
                      <th class="text-left px-5 py-5 body-2 font-weight-bold text-uppercase">
                        1 Days
                      </th>

                      <!-- <th class="text-left px-5 py-5 body-2 font-weight-bold text-uppercase">
                        1 Weeks
                      </th>

                      <th class="text-left px-5 py-5 body-2 font-weight-bold text-uppercase">
                        1 Month
                      </th> -->

                      <th class="text-left px-5 py-5 body-2 font-weight-bold text-uppercase">
                        1 Years
                      </th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="item in desserts" :key="item.name">
                      <td class=" py-3">

                        <v-list-item class="grow">
                          <v-list-item-avatar>
                            <v-img  contain class="elevation-6" alt="" :src="item.img"></v-img>
                          </v-list-item-avatar>

                          <v-list-item-content>
                            <v-list-item-title class="font-weight-bold"> {{ item.name }} </v-list-item-title>
                          </v-list-item-content>
                        </v-list-item>

                      </td>
                      <td class="text-left">{{ item.prices }}</td>
                
                      <td :class="item.daysColors">{{ item.days }}</td>
                      <!-- <td>{{ item.weeks }}</td>
                      <td>{{ item.month }}</td> -->
                      <td :class="item.yearsColors">{{ item.years }}</td>
                    </tr>
                  </tbody>
                </template>
              </v-simple-table>
            </v-container>
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
          title: 'Start Investing ',
          span: 'Now',
          desc: 'Cryptocurrency is a digital asset that is secured using cryptography on an open database called blockchain. There are 2 types of crypto, namely coin and token'
        }],
        desserts: [{
            name: 'Bitcoins',
            img: 'https://cryptologos.cc/logos/bitcoin-btc-logo.svg',
            prices: '$36,036.50 ',
            daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
          },
          {
            name: 'Ethereum',
            img: 'https://cryptologos.cc/logos/ethereum-eth-logo.svg?v=018',
            prices: '$ 2,380.20 ',
          daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
          },
          {
            name: 'Binance Coins',
            img: 'https://cryptologos.cc/logos/binance-coin-bnb-logo.svg?v=018',
            prices: '$ 359,27 ',
               daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
           
           
            years: '100%',
          },
          {
            name: 'Tether Usdts',
            img: 'https://cryptologos.cc/logos/tether-usdt-logo.svg?v=018',
            prices: '$ 150 ',
             daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
          },
          {
            name: 'Solana',
            img: 'https://cryptologos.cc/logos/solana-sol-logo.svg?v=018',
            prices: '$ 150 ',
            daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
          },
             {
            name: 'Cardano',
            img: 'https://cryptologos.cc/logos/cardano-ada-logo.svg?v=0188',
            prices: '$ 150 ',
            daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
          },
             {
            name: 'Decentraland',
            img: 'https://cryptologos.cc/logos/decentraland-mana-logo.svg?v=018',
            prices: '$ 150 ',
               daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
           
         
          },
             {
            name: 'Sandbox',
            img: 'https://cryptologos.cc/logos/the-sandbox-sand-logo.svg?v=018',
            prices: '$ 150 ',
         daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
          },
          {
            name: 'Shiba Inu',
            img: 'https://cryptologos.cc/logos/shiba-inu-shib-logo.svg?v=018',
            prices: '$ 150 ',
         daysColors: 'red--text text--lighten-1',
              days: '- 18%',
            yearsColors: 'green--text text--lighten-1',
            years: '+ 110%',
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
