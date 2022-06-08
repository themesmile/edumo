<template>

  <div>

    <div class="area">
      <ul class="circles">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </div>
  </div>

</template>

<style lang="scss">
  @import './coin-bg';
</style>

<script>
  import BlogCard from '../Cards/BlogCard'
  import ScrollWrap from '../ScrollWrap'
  import accountBg from '~/static/images/cta-bg.svg'
  import GoogleStore from '~/static/images/google-playstore.svg'
  import AppStore from '~/static/images/app-store.svg'

  export default {
    components: {
      BlogCard,
      ScrollWrap
    },
    data() {
      return {
        accountBg: accountBg,
        GoogleStore: GoogleStore,
        AppStore: AppStore,
        blogData: [

          {
            img: "https://source.unsplash.com/random",

            title: 'How To Grow Your Crypto Portfolio with Recurring Buy',
            desc: 'This is a media card. You can use this section to describe the content.'
          },
          {
            img: "https://source.unsplash.com/random/?city,night",
            title: '12 Money Challenges For A Year Of Fun Saving',
            desc: 'This is a media card. You can use this section to describe the content.'
          },
          {
            img: "https://source.unsplash.com/random/?technology",
            title: 'Stablecoins: What, Why & How To Buy Them',
            desc: 'This is a media card. You can use this section to describe the content.'
          },
          {
            img: "https://source.unsplash.com/random/?3d-renders",
            title: 'The Perfect Time For Passive Income With Crypto',
            desc: 'This is a media card. You can use this section to describe the content.'
          }
        ]
      }
    }
  }
</script>
