<template>
  <v-container class="mb-16">
    <p class="body-1 text-center mb-6 mt-16 pt-16">
      Frequently Asked <span>Questions</span>
    </p>
    <h3 class="display-1 font-weight-bold text-center mb-6 ">
      Want to ask something<br>from us?
    </h3>
    <v-row justify="center" class="mt-12">
      <v-col md="10" sm="12" cols="12" lg="10">
        <v-expansion-panels flat class="mb-4">
          <v-expansion-panel>
            <v-expansion-panel-header disable-icon-rotate class="font-weight-bold" expand-icon>
              <template v-slot:actions>
                <v-icon color="primary">
                  add_box
                </v-icon>
              </template>
              How do I make a yearly payment?
            </v-expansion-panel-header>
            <v-expansion-panel-content class="body-2">
              Serenity Is Multi-Faceted Blockchain Based Ecosystem, Energy Retailer For The People, Focusing On The
              Promotion Of Sustainable Living, Renewable Energy Production And Smart Energy Grid Utility Services.
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>

        <v-expansion-panels flat class="mb-4">
          <v-expansion-panel>
            <v-expansion-panel-header disable-icon-rotate class="font-weight-bold" expand-icon>
              <template v-slot:actions>
                <v-icon color="primary">
                  add_box
                </v-icon>
              </template>
              How do I make a yearly payment?
            </v-expansion-panel-header>
            <v-expansion-panel-content class="body-2">
              Duis Aute Irure Dolor In Reprehenderit In Voluptate Velit Esse Cillum Dolore Eu Fugiat Nulla Pariatur.
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>

        <v-expansion-panels flat class="mb-4">
          <v-expansion-panel>
            <v-expansion-panel-header disable-icon-rotate class="font-weight-bold" expand-icon>
              <template v-slot:actions>
                <v-icon color="primary">
                  add_box
                </v-icon>
              </template>
              How this technology works?
            </v-expansion-panel-header>
            <v-expansion-panel-content class="body-2">
              Serenity Is Multi-Faceted Blockchain Based Ecosystem, Energy Retailer For The People, Focusing On The
              Promotion Of Sustainable Living, Renewable Energy Production And Smart Energy Grid Utility Services.
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>

        <v-expansion-panels flat class="mb-4">
          <v-expansion-panel>
            <v-expansion-panel-header disable-icon-rotate class="font-weight-bold">
              <template v-slot:actions>
                <v-icon color="primary">
                  add_box
                </v-icon>
              </template>
              How to contact with Customer Service?
            </v-expansion-panel-header>
            <v-expansion-panel-content class="body-2">
              Duis Aute Irure Dolor In Reprehenderit In Voluptate Velit Esse Cillum Dolore Eu Fugiat Nulla Pariatur.
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>

        <v-expansion-panels flat class="mb-4">
          <v-expansion-panel>
            <v-expansion-panel-header disable-icon-rotate class="font-weight-bold">
              <template v-slot:actions>
                <v-icon color="primary">
                  add_box
                </v-icon>
              </template>
              Website reponse taking time, how to improve?
            </v-expansion-panel-header>
            <v-expansion-panel-content expand class="body-2">
              Duis Aute Irure Dolor In Reprehenderit In Voluptate Velit Esse Cillum Dolore Eu Fugiat Nulla Pariatur
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>
    </v-row>



  </v-container>
</template>

<style lang="scss">
  @import './faq-style';
</style>

<script>
  import PricingCard from '../Cards/PricingCard'
  import accountBg from '~/static/images/cta-bg.svg'
  import GoogleStore from '~/static/images/google-playstore.svg'
  import AppStore from '~/static/images/app-store.svg'
  export default {
    components: {
      PricingCard
    },
    data() {
      return {
        accountBg: accountBg,
        GoogleStore: GoogleStore,
        AppStore: AppStore
      }
    }
  }
</script>
