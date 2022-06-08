<template>
  <div>
    <h1 class="mt-16 pt-16 md-mt-0 md-pt-0 text-center font-weight-bold text-sm-h5 text-lg-h3 ">{{ title }} <span
        class=" font-weight-bold primary--text text--darken-2">{{ span }}</span>
    </h1>
    <h3 class="mt-8  text-center title">{{ desc }}.</h3>
  </div>
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
      span: {
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
