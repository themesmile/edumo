<template>
  <div class="comparison-cryptogate pt-12 ">
    <v-row class="d-flex align-center pt-12 ">
      <v-col ols="12" sm="12" md="12" lg="12" class="pa-2 pr-4">
        <h3 class="display-1 font-weight-bold text-capitalize text-center mt-16 mb-2">Same principal, higher returns
        </h3>
        <h5 class="title font-weight-medium text-capitalize text-center mb-3">See the potential returns of crypto
          investments
        </h5>
      </v-col>
    </v-row>
    <v-row class="d-flex align-center">

      <v-col cols="12" sm="12" md="3" lg="3" class="pa-2">
        <v-progress-linear value="30" rounded class="justify-start pl-2 my-6" height="60" color="#0065F2">
          <span class="progress-bar-icons material-icons-round">
            account_balance
          </span>
          <span class="progress-bar-txt body-2 ">
            Deposit
          </span>
          <span class=" progress-bar-price font-weight-black body-1">
            $1.050
            <v-chip class="ma-2" color="primary">
              + 5.5%
            </v-chip>
          </span>
        </v-progress-linear>
      </v-col>

      <v-col cols="12" sm="12" md="3" lg="3" class="pa-2">
        <v-progress-linear value="70" rounded class="justify-start pl-2 my-6" height="60" color="#FFCD1B">
          <span class="progress-bar-icons material-icons-round">
            stacked_bar_chart
          </span>
          <span class="progress-bar-txt body-2 ">
            Gold
          </span>
          <span class=" progress-bar-price font-weight-black body-1">
            $1.277
            <v-chip class="ma-2" color="#FFCD1B">+ 27.7%</v-chip>
          </span>
        </v-progress-linear>
      </v-col>


      <v-col cols="12" sm="12" md="3" lg="3" class="pa-2">
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


      </v-col>
      <v-col cols="12" sm="12" md="3" lg="3" class="pa-2">


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
    <p class="caption text-center">Comparison of $ 1.000 investment (Funds invested on 1 January 2020). Return
      calculations are based on to the value of each asset as of 31 December
      2020.</p>
  </div>

</template>

<style lang="scss">
  @import './comparison-two';
</style>
<script>
  export default {
    components: {}
  }
</script>
