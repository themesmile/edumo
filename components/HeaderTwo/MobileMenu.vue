<template>
  <div>

    <br>
    <v-list-item v-for="item in MainItems" :key="item.title" dense @click="$router({path: item.route})">
      <v-btn text class="mobile-menu-cryptogate menu-list px-0 text-left mx-0 body-2 mb-4" :to="item.link">
        {{ item.title }}
      </v-btn>
    </v-list-item>



    <v-list rounded>
      <v-list-group :value="true">
        <template v-slot:activator>
          <v-list-item-title class="menu-list">Page</v-list-item-title>
        </template>
        <v-list>
          <v-list-item v-for="(item, index) in items" :key="index" :href="item.link">
            <v-list-item-title class="menu-list">{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-list-group>
    </v-list>
    <v-divider />
    <v-list rounded>
      <v-list-item v-for="(item, index) in ['Login', 'Connect Wallet']" :key="index" :href="'/' + item" link>
        <v-list-item-content>
          <v-list-item-title class="menu-list">{{ item }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>

  </div>
</template>

<style lang="scss">
  @import './header-style';
</style>

<script>
  import navMenu from './menu'

  export default {
    data() {
      return {
        MainItems: [{
            icon: 'mdi-speedometer',
            title: 'Home',
            link: '/#home'
          },
          {
            icon: 'mdi-speedometer',
            title: 'Feature',
            link: '/#feature'
          },
          {
            icon: 'mdi-speedometer',
            title: 'Testimonials',
            link: '/#testimonials'
          },
          {
            icon: 'mdi-speedometer',
            title: 'Faq',
            link: '/#faq'
          },
          {
            icon: 'mdi-speedometer',
            title: 'Subscribe',
            link: '/#subscribe'
          }
        ],
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
        navMenu: navMenu,
        isOpen: false
      }
    }
  }
</script>
