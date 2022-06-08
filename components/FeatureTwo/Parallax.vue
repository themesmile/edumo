<template>
  <div class="parallax-wrap">
    <v-container>
      <div class="banner-parallax-wrap" v-if="loaded">
        <div class="figure">
          <div>
            <parallax
              :speed-factor="0.2"
              direction="down"
            >
              <svg
                width="600px"
                height="800px"
                class="parallax-vertical parallax-dot"
              >
                <use xlink:href="/images/decoration/dot-deco.svg#dot" />
              </svg>
            </parallax>
          </div>
        </div>


      </div>
    </v-container>
  </div>
</template>

<style lang="scss">
@import './feature-styles';
</style>

<script>
import Parallax from 'vue-parallaxy'
export default {
  components: {
    Parallax
  },
  data: () => ({
    loaded: false
  }),
  mounted() {
    this.loaded = true
  }
}
</script>
