<template>


    <v-row justify="center" class="d-flex align-center pt-12 justify-center" :class="reverse">
      <v-col md="7" sm="12" cols="12" lg="7" class="lg-px-12 sm-px-0 md-px-12">
        <h1 class="mb-4 text-h4 font-weight-bold"> {{ title }}</h1>
        <p>{{ desc }}</p>
        <v-btn depressed color="rgba(0,0,0,0.8)" dark large rounded class="comparison-button text-capitalize px-6 mt-6">
          Learn More
          <v-icon class="ml-4">arrow_forward</v-icon>
        </v-btn>
      </v-col>
      <v-col md="5" sm="12" cols="12" lg="5">
        <v-img class="rounded-xl" :src="img" height="400px" />
      </v-col>
    </v-row>



</template>

<style lang="scss">
  @import './card-styles';
</style>

<script>
  export default {
    props: {
      reverse: {
        type: String,
        required: true
      },
      img: {
        type: String,
        required: true
      },
      title: {
        type: String,
        required: true
      },
      desc: {
        type: String,
        required: true
      }
    }
  }
</script>
