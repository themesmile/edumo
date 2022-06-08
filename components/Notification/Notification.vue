<template>
  <v-snackbar
    :timeout="-1"
    v-model="snackbar"
    flat
    class="notification"
  >
    <div class="action pr-12">
      {{ msgNotif }}
    </div>
        <v-btn
      outlined
      color="white"
      class="button overline px-10"
      rounded

    >
 
   {{ $t('common.accept') }} 
    </v-btn>

          <v-btn
        class="ma-2"
        text
        icon
        color="red lighten-2"
        @click="snackbar = false"
      >
        <v-icon>close</v-icon>
      </v-btn>
  </v-snackbar>
</template>

<style lang="scss" scoped>
@import './notification-style.scss';
</style>

<script>
import brand from '~/static/text/brand'

export default {
  data() {
    return {
      snackbar: true,
      msgNotif: brand.starter.notifMsg
    }
  }
}
</script>
