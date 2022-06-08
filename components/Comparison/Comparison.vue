<template>
  <div class="comparison-cryptogate pt-12 ">
    <v-row justify="center" class="mb-12">
      <v-col md="8" sm="8" cols="8" lg="8" class="pa-2 pr-4">


        <v-chip class="overline font-weight-medium  text-center mb-4 ma-2" color="primary">
          <v-icon left>
            mdi-account-circle-outline
          </v-icon>
          higher returns
        </v-chip>
        <h2 class="font-weight-medium display-1 font-weight-bold mb-4 text-center text-capitalize cryptogate-title"> See
          the potential returns of crypto
          investments
        </h2>

        <p class="body-2 text-center">Comparison of $ 1.000 investment (Funds invested on 1 January 2020). Return
          calculations are based on to the value of each asset as of 31 December
          2020.</p>
      </v-col>
    </v-row>
    <v-row class="d-flex align-center">

      <v-col cols="12" sm="12" md="12" lg="6" class="pa-2">

        <v-card class="mx-auto pa-6">
          <v-list-item three-line>

            <v-progress-circular :value="80" :size="100" color="primary lighten-2" class="mr-4">
              <span class="progress-bar-icons material-icons-round">
                account_balance
              </span>
            </v-progress-circular>
            <v-list-item-content>

              <v-list-item-title>
                Deposit
              </v-list-item-title>
              <v-list-item-subtitle>A deposit is a financial term that means money held at a bank. A deposit is a
                transaction involving a transfer of money to another party for safekeeping.</v-list-item-subtitle>
              <v-spacer></v-spacer>
              <span class=" progress-bar-price font-weight-black body-1">
                <v-chip class="ma-0" color="green">
                  Result $1.050
                </v-chip>

                <v-chip class="ma-2" color="primary">
                  + 5.5%
                </v-chip>
              </span>
            </v-list-item-content>


          </v-list-item>


        </v-card>

        <v-card class="mx-auto pa-6 mt-6">
          <v-list-item three-line>

            <v-progress-circular :value="80" :size="100" color="#FFCD1B" class="mr-4">
              <span class="progress-bar-icons material-icons-round">
                stacked_bar_chart
              </span>
            </v-progress-circular>
            <v-list-item-content>

              <v-list-item-title class="mb-3">
                Gold
              </v-list-item-title>
              <v-list-item-subtitle class="mb-3">A deposit is a financial term that means money held at a bank. A
                deposit is a transaction involving a transfer of money to another party for safekeeping.
              </v-list-item-subtitle>
              <v-spacer></v-spacer>
              <span class=" progress-bar-price font-weight-black body-1">
                <v-chip class="ma-0" color="#FFCD1B lighten-2">
                  Result $1.050
                </v-chip>

                <v-chip class="ma-2" color="#FFCD1B">
                  + 5.5%
                </v-chip>
              </span>
            </v-list-item-content>


          </v-list-item>


        </v-card>


        <v-progress-linear value="70" rounded class="justify-start pl-2 my-6" height="60" color="#FFCD1B">

          <span class="progress-bar-txt body-2 ">
            Gold
          </span>
          <span class=" progress-bar-price font-weight-black body-1">
            $1.277
            <v-chip class="ma-2" color="#FFCD1B">+ 27.7%</v-chip>
          </span>
        </v-progress-linear>


      </v-col>

      <v-col cols="12" sm="12" md="12" lg="6" class="pa-2">
        <v-progress-linear value="20" rounded class="justify-start pl-2 my-6" height="60" color="#00C487">
          <span class="progress-bar-icons material-icons-round">
            request_quote
          </span>
          <span class="progress-bar-txt">
            Dollar
          </span>

          <span class=" progress-bar-price font-weight-black body-1">
            $1.022
            <v-chip class="ma-2" color="#00C487">+ 2%</v-chip>
          </span>
        </v-progress-linear>


        <v-progress-linear value="300" rounded class="justify-start pl-2 my-6" height="60" color="#FFA41B">
          <span class="progress-bar-icons material-icons-round">
            currency_bitcoin
          </span>
          <span class="progress-bar-txt">
            Bitcoin
          </span>
          <span class=" progress-bar-price font-weight-black body-1">
            $3.000
            <v-chip class="ma-2" color="rgba(0,0,0,0.2)">+ 300%</v-chip>
          </span>
        </v-progress-linear>

      </v-col>
    </v-row>

  </div>


</template>

<style lang="scss">
  @import './comparison';
</style>
<script>
  import logo from '~/static/images/phone-crypto.png'
  export default {
    components: {},
    data() {
      return {
        logo: logo
      }
    }
  }
</script>
