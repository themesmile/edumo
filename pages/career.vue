<template>
  <div>

    <div class="main-wrap">
      <main-header class="main-header" />
      <main class="container-wrap">


        <section id="security" class="security">
          <v-parallax class="parallax-crypto" :src="featureBg ">
            <v-container>

              <v-row justify="center" class="mb-12">
                <v-col md="10" sm="10" cols="10" lg="8">
                  <div v-for="(item, index) in HeadlineData" :key="index">
                    <page-headline :title="item.title" :span="item.span" :desc="item.desc" />
                  </div>
                </v-col>
              </v-row>
              <v-row justify="center">
                <v-col md="12" sm="12" lg="10" cols="10">
                   <div v-for="(item, index) in TimelineData" :key="index">
                        <timeline-card flat :title="item.title" :desc="item.desc" :img="item.img" :reverse="item.reverse" />
                      </div>
                </v-col>
              </v-row>
              <div id="blog-list" class="blog-wrap mt-16">
                <span class="text-left headline font-weight-bold mb-6">Choose Your Team</span>
                <p class="body-1">Select a team most relevant to your interests and experience to view job openings.</p>
                <v-row justify="center">
                  <v-col md="12" cols="12">
                    <v-row>
                      <v-col v-for="(item, index) in blogData" :key="index" md="4" lg="4" cols="12" class="px-4">
                        <security-card flat :title="item.title" :desc="item.desc" :more="item.more" />
                      </v-col>
                    </v-row>
                  </v-col>
                </v-row>
              </div>
            </v-container>
          </v-parallax>
        </section>


      </main>

      <section id="faq" class="space-top account-bg-color">
        <v-parallax class="parallax-crypto" :src="accountBg">
          <Subscribe />
          <main-footer />

        </v-parallax>
      </section>
    </div>
  </div>
</template>

<style lang="scss">
  @import './main';
</style>

<script>
  import HeaderTwo from '~/components/HeaderTwo'
  import Hidden from '~/components/Hidden'
  import Subscribe from '~/components/Subscribe'
  import Footer from '~/components/Footer'
  import PageNav from '~/components/PageNav'
  import Notification from '~/components/Notification'
  import brand from '~/static/text/brand'
  import featureBg from '~/static/images/feature-bg.svg'
  import homeBg from '~/static/images/home-bg.svg'
  import accountBg from '~/static/images/account-bg.svg'

  import TimelineCard from '~/components/Cards/TimelineCard'
   import SecurityCard from '~/components/Cards/SecurityCard'
  import PageHeadline from '~/components/Cards/PageHeadline'
  export default {
    components: {
      'main-header': HeaderTwo,
      Hidden,
      TimelineCard,
       SecurityCard,
      PageHeadline,
      Subscribe,
      PageNav,
      Notification,
      'main-footer': Footer
    },
    data() {
      return {
        featureBg: featureBg,
        homeBg: homeBg,
        accountBg: accountBg,
        HeadlineData: [{
          title: 'We’re on a mission to accelerate transition to an',
          span: 'open financial system',
          desc: 'Let’s work together! We’ve saved a seat for you.'

        }],
         TimelineData: [
           {
          title: 'Thrive with Cryptogate',
          img: 'https://source.unsplash.com/random/?computer',
          desc: 'What is our secret to success? Our people. Be united by a commom DNA of talented, hardworking and passionate individuals in a world renowned team.',
          reverse: 'flex-row-reverse'
        },
                 {
          title: 'Inspire through Innovation',
          img: 'https://source.unsplash.com/random/?3d',
          desc: 'Embrace the future with challenges. Tackle accelerating the adoption of cryptocurrency, blockchain, and distributed ledger technology with the leading company in the crypto space.'
        },
                      {
          title: 'Inspire through Innovation',
          reverse: 'flex-row-reverse',
          img: 'https://source.unsplash.com/random/?technologies',
          desc: 'Embrace the future with challenges. Tackle accelerating the adoption of cryptocurrency, blockchain, and distributed ledger technology with the leading company in the crypto space.'
        }
        ],
        blogData: [{
            title: 'Frontend Developer',
            more: 'Apply Now',
            desc: 'Associate / Supervisor.'

          },
          {
            title: 'Backend Developer',
            desc: 'Fresh Graduate',
            more: 'Apply Now'
          },
          {
            title: 'UI / UX Designer',
            desc: 'Fresh Graduate / Entry Level',
            more: 'Apply Now'
          },
          {
            title: 'Frontend Developer',
            desc: 'Fresh Graduate',
            more: 'Apply Now'
          },
          {
            title: 'Data Analyst',
            desc: 'Associate / Supervisor.',
            more: 'Are You Ready'
          }
        ]
      }
    },
    head() {
      return {
        title: brand.starter.name + ' - Career'
      }
    }
  }
</script>
