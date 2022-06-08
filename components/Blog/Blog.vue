<template>

 
    <scroll-wrap target="blog-list">
      
      <h3 class="display-2 font-weight-bold text-center text-center mb-4 mt-16 pt-16">
        Latest Updates

      </h3>
      <p class="body-1 text-center mb-14">
        All the latest news and updates about Phantom the product, the company, and the team
      </p>
      <div
        id="blog-list"
        class="blog-wrap"
      >
        <v-row justify="center">
          <v-col md="11" cols="11">
            <v-row>
              <v-col
                v-for="(item, index) in blogData"
                :key="index"
                md="3"
                cols="12"
                class="px-4"
              >
                <blog-card
               
                  :width="item.width"
                  :title="item.title"
                  :desc="item.desc"
                  :img="item.img"
                />
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </div>
    </scroll-wrap>
  
</template>

<style lang="scss">
@import './blog-style';
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
          desc:
            'This is a media card. You can use this section to describe the content.'
        },
        {
          img: "https://source.unsplash.com/random/?city,night",
          title: '12 Money Challenges For A Year Of Fun Saving',
          desc:
            'This is a media card. You can use this section to describe the content.'
        },
          {
            img: "https://source.unsplash.com/random/?technology",
          title: 'Stablecoins: What, Why & How To Buy Them',
          desc:
            'This is a media card. You can use this section to describe the content.'
        },
        {
             img: "https://source.unsplash.com/random/?3d-renders",
          title: 'The Perfect Time For Passive Income With Crypto',
          desc:
            'This is a media card. You can use this section to describe the content.'
        }
      ]
    }
  }
}
</script>
