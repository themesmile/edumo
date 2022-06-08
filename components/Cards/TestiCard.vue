<template>
  <v-card class="card pa-12">
    <p class="body1">
      {{ text }}
    </p>
    <v-row class="d-flex justify-start my-3 ml-0">
      <v-icon class='material-icons-round' color="primary">star</v-icon>
      <v-icon class='material-icons-round' color="primary">star</v-icon>
      <v-icon class='material-icons-round' color="primary">star</v-icon>
      <v-icon class='material-icons-round' color="primary">star</v-icon>
      <v-icon class='material-icons-round'>star</v-icon>
    </v-row>
    <div class="name pt-4">
      <v-avatar :size="36" class="avatar">
        <img :src="avatar" :alt="name">
      </v-avatar>

      <span class="caption">
        {{ name }}
      </span>
    </div>

  </v-card>
</template>

<style lang="scss">
  @import './card-styles';
</style>

<script>
  export default {

    props: {
      text: {
        type: String,
        required: true
      },
      avatar: {
        type: String,
        required: true
      },
      name: {
        type: String,
        required: true
      }
    }
  }
</script>
