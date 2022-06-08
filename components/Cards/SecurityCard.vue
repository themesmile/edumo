<template>
  <v-card
    class="mx-auto"
    max-width="500"
  >
    <v-card-title class="font-weight-bold headline px-10 pt-10">
      {{ title }}
    </v-card-title>
    <v-card-text class="px-10">
      <span class="text--primary">
        <span>{{ desc }}</span>
      </span>
    </v-card-text>
    <v-card-actions class="px-10 pb-10">
           <v-btn depressed color="rgba(0,0,0,0.4)" dark large rounded class="comparison-button text-capitalize">
          {{ more }}

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
    img: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
      more: {
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
