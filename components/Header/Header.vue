<template>
  <div>
    <v-navigation-drawer v-if="isTablet" v-model="openNavMobile" fixed temporary class="mobile-nav">
      <mobile-menu />
    </v-navigation-drawer>
    <v-app-bar v-scroll="handleScroll" :class="{ fixed: fixed }" class="header" fixed app height="auto">

      <div class="header-content">
        <nav class="nav-menu">
          <v-btn v-if="isTablet" text icon @click.stop="handleToggleOpen">
            <v-icon>menu</v-icon>
          </v-btn>
          <div class="logo">
              <NuxtLink to="/">
              <img :src="logo" alt="logo">
            </NuxtLink>
          </div>
          <div v-if="loaded" class="d-flex justify-center">
            <scrollactive v-if="isDesktop" :offset="navOffset" active-class="active" tag="div">
              <v-btn v-for="(item, index) in menuList" :key="index" :href="item.url"
                class="anchor-link scrollactive-item overline font-weight-bold px-4" text rounded
                @click="setOffset(item.offset)">
                {{ item.name }}
              </v-btn>
              <v-menu transition="slide-y-transition" offset-y nudge-top="-30" bottom class="menu-setting">
                <template v-slot:activator="{ on, attrs }">
                  <v-btn text class="overline font-weight-bold px-4" dark rounded v-bind="attrs" v-on="on">
                    Page
                     <v-icon>arrow_drop_down</v-icon>
                  </v-btn>
                </template>
                <v-list>
                  <v-list-item v-for="(item, index) in items" :key="index" :href="item.link">
                    <v-list-item-title class="cryptogate-letterspacing overline font-weight-bold px-4">{{ item.title }}
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-menu>
            </scrollactive>
          </div>
        </nav>
        <nav class="user-menu ">
          <v-btn rounded depressed v-if="isDesktop" text class="anchor-link scrollactive-item overline font-weight-bold px-4 d-none d-sm-flex" to="/login">
            Login
          </v-btn>

 <ConnectWallet />



          <v-spacer v-if="isDesktop" class="vertical-divider" />
          <setting-menu />
        </nav>
      </div>

    </v-app-bar>
  </div>
</template>

<style lang="scss" scoped>
  @import './header-style.scss';
</style>

<script>
  import logo from '~/static/images/cryptogate-logo.svg'
  import navMenu from './menu'
  import Settings from './Settings'
  import MobileMenu from './MobileMenu'
import ConnectWallet from '~/components/ConnectWallet'
  let counter = 0

  function createData(name, url, offset) {
    counter += 1
    return {
      id: counter,
      name,
      url,
      offset
    }
  }

  export default {
    components: {
      'setting-menu': Settings,
      ConnectWallet,
      MobileMenu
    },

    data() {
      return {

        items: [{
            title: 'Home 1',
            icon: 'mdi-account-circle',
            link: "/"
          },
          {
            title: 'Home 2',
            icon: 'mdi-account-circle',
            link: "/index-two"
          },
          {
            title: 'Market',
            icon: 'mdi-account-circle',
            link: "/market"
          },
          {
            title: 'Security',
            icon: 'mdi-account-circle',
            link: "/security"
          },
          {
            title: 'Blog',
            icon: 'mdi-account-circle',
            link: "/blog"
          },
          {
            title: 'Career',
            icon: 'shopping_bag',
            link: "/career"
          },

        ],
        logo: logo,
        section: 0,
        fixed: false,
        loaded: false,
        openNavMobile: null,
        navOffset: 20,
        menuList: [
          createData(navMenu[0], '#' + navMenu[0]),
          createData(navMenu[1], '#' + navMenu[1]),
          createData(navMenu[2], '#' + navMenu[2]),
          createData(navMenu[3], '#' + navMenu[3], -40),
          createData(navMenu[4], '#' + navMenu[4], -40)
        ]
      }
    },
    mounted() {
      this.loaded = true
    },
    methods: {
      handleScroll: function () {
        if (window.scrollY > 280) {
          return (this.fixed = true)
        }
        return (this.fixed = false)
      },
      setOffset: function (offset) {
        this.navOffset = offset
      },
      handleToggleOpen: function () {
        this.openNavMobile = !this.openNavMobile
      }
    },
    computed: {
      isTablet() {
        const mdDown = this.$store.state.breakpoints.mdDown
        return mdDown.indexOf(this.$mq) > -1
      },
      isDesktop() {
        const lgUp = this.$store.state.breakpoints.lgUp
        return lgUp.indexOf(this.$mq) > -1
      }
    }
  }
</script>
