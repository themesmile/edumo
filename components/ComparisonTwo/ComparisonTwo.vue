<template>
  <div class="comparison-cryptogate pt-12 ">

    <v-row justify="center" class="mb-12 text-center ">
      <v-col md="6" sm="6" cols="6" lg="6" class="pa-2 pr-4">
        <h2 class="font-weight-medium display-1 mb-3 p-10"><span class="font-weight-bold indigo--text">Edumo</span> is
          digital learning company that we<br> provide a way for online learning platform </h2>
        <p class="body-1 mt-5"> Our business focuses on providing service for clients who want to move from traditional,
          boring, offline learning to a digital-based learning with full online or hybrid method. </p>
      </v-col>
    </v-row>
    <v-row justify="space-around">
      <v-btn color="white" depressed large rounded class="comparison-button text-capitalize">
        Selengkapnya
        <v-icon class="ml-4">arrow_forward</v-icon>
      </v-btn>
    </v-row>


    <v-row justify="center" class="mb-12 text-left mt-12">

      <v-col cols="4" sm="4" md="4" lg="4" class="pa-2">

        <v-list-item class="mb-8">

          <v-list-item-avatar size="90">
            <v-img :src="avatar"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>

            <v-list-item-title class="title font-weight-bold mb-2">
              Experts lecture
            </v-list-item-title>
            <v-list-item-subtitle>Help to employees reach the goals from an experts lecture</v-list-item-subtitle>


          </v-list-item-content>
        </v-list-item>



        <v-list-item>

          <v-list-item-avatar size="90">
            <v-img :src="various"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>

            <v-list-item-title class="title font-weight-bold mb-2">
              Various category 
            </v-list-item-title>
            <v-list-item-subtitle>Various category to
improve your skill
</v-list-item-subtitle>


          </v-list-item-content>
        </v-list-item>




      </v-col>


      <v-col cols="4" sm="4" md="4" lg="4" class="pa-2">


        <v-list-item class="mb-8">

          <v-list-item-avatar size="90">
            <v-img :src="intensive"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>

            <v-list-item-title class="title font-weight-bold mb-2">
              Intensive program
            </v-list-item-title>
            <v-list-item-subtitle>Intensive program to boost 
your result</v-list-item-subtitle>


          </v-list-item-content>
        </v-list-item>

        <v-list-item>

          <v-list-item-avatar size="90">
            <v-img :src="flexible"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>

            <v-list-item-title class="title font-weight-bold mb-2 title-line">
              Flexible time
            </v-list-item-title>
            <v-list-item-subtitle>Flexible time & content create</v-list-item-subtitle>


          </v-list-item-content>
        </v-list-item>





      </v-col>

    </v-row>

  </div>

</template>

<style lang="scss">
  @import './comparison-two';
</style>
<script>
  import avatar from '~/static/images/lecture.svg'
  import intensive from '~/static/images/intensive.svg'
  import various from '~/static/images/various.svg'
    import flexible from '~/static/images/flexible.svg'

  export default {
    components: {},
    data() {
      return {
        avatar: avatar,
        intensive: intensive,
        various: various,
        flexible: flexible,

      }
    }
  }
</script>
