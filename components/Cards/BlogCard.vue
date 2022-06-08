<template>
  <v-card
    class="mx-auto"
    :max-width="width"
  >
    <v-img
      :src="img"
      class="white--text"
      height="300px"
    />
    <v-card-title class="font-weight-bold px-10 pt-10">
      {{ title }}
    </v-card-title>
    <v-card-text class="px-10">
      <span class="text--primary">
        <span>{{ desc }}</span>
      </span>
    </v-card-text>
    <v-card-actions class="px-10 pb-10">
       <v-btn depressed color="rgba(0,0,0,0.2)" dark medium rounded class="comparison-button text-capitalize px-6">
          Read More
          <v-icon class="ml-4">arrow_forward</v-icon>
        </v-btn>
    </v-card-actions>
  </v-card>
</template>

<style lang="scss">
@import './card-styles';
</style>

<script>
export default {
  props: {
    width:{
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
