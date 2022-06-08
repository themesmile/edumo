<template>


  <div class="text-center">
    <v-dialog v-model="dialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <v-btn rounded depressed class="overline font-weight-bold d-none d-sm-flex" color="primary" dark v-bind="attrs"
          v-on="on">
          Connect Wallet
        </v-btn>
      </template>

      <v-card class="rounded-xl py-10 px-10">
        <v-list rounded>
          <v-title class="text-h5 font-weight-bold mb-5">
            Sign in with your wallet
          </v-title>
          <br>
          <v-subheader class="pa-0 ma-0">

            Sign in with one of available wallet providers or create a new wallet. What is a wallet?

          </v-subheader>
          <v-list-item-group class="mt-6" v-model="selectedItem" color="primary">
            <v-list-item v-for="(item, i) in itemsWallet" :key="i">
              <v-list-item-icon>


                <v-avatar contain tile>
                  <img class="py-1 px-1" contain :src="item.img" alt="John" size="128">

                </v-avatar>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item-content>

              <v-list-item-action>

                <v-chip class="ma-2" :color="item.color" :text-color="item.textColor">
                  {{ item.name }}
                </v-chip>

              </v-list-item-action>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-card>




    </v-dialog>
  </div>


</template>

<style lang="scss">
  @import './subscribe-style';
</style>
<script>
  import imgAPI from '~/static/images/imgAPI'
  export default {
    data() {
      return {
        itemsWallet: [{
            text: 'Metamask',
            name: 'Popular',
            color: 'primary',
            textColor: 'white',
            img: 'https://rarible.com/3ca93659526bbbdf7bca.svg'
          },
          {
            text: 'Torus',
            name: 'Tezos',
            color: 'rgba(56, 128, 255, 0.1)',
            textColor: '#3880ff',
            img: 'https://rarible.com/6eb10dd4202620a6d06e.svg'
          },
          {
            text: 'Conversions',
            name: 'Flow',
            color: 'rgba(0, 216, 22, 0.1)',
            textColor: 'rgba(0, 216, 22, 1)',
            img: 'https://rarible.com/970342d3c19a87a56dba.svg'
          },

        ],
        message1: 'yourname@hosting.com',
        partner01: imgAPI.partners[1],
        partner02: imgAPI.partners[2],
        partner03: imgAPI.partners[3],
        partner04: imgAPI.partners[4],
        partner05: imgAPI.partners[5],
        partner06: imgAPI.partners[6],
      }
    }
  }
</script>
