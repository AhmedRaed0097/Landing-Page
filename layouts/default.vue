<template>
  <v-app>
    <v-navigation-drawer
      v-if="$vuetify.breakpoint.mobile"
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
    :color="isScrolling === true ? '#f00' : 'transparent'"
    :clipped-left="clipped" fixed app>
      <div class="larg-nav-container">
        <div class="logo">
          <h1>MySite</h1>
        </div>
        <v-list v-if="!$vuetify.breakpoint.mobile">
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :to="item.to"
            router
            exact
          >
            <v-list-item-content>
              <v-list-item-title v-text="item.title" />
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </div>

      <v-spacer />
      <v-btn icon @click.stop="drawer = !drawer">
        <v-icon v-if="$vuetify.breakpoint.mobile">mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      isScrolling: false,
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Home",
          to: "/",
        },
        {
          icon: "mdi-apps",
          title: "Services",
          to: "/service",
        },
        {
          icon: "mdi-apps",
          title: "Work",
          to: "/work",
        },
        {
          icon: "mdi-apps",
          title: "Blog",
          to: "/blog",
        },
        {
          icon: "mdi-apps",
          title: "Pricing",
          to: "/pricing",
        },
        {
          icon: "mdi-apps",
          title: "Team",
          to: "/team",
        },
        {
          icon: "mdi-apps",
          title: "Contact",
          to: "/contact",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
  methods:{

    handleScroll(event) {
      if (window.scrollY > 0) {
        this.isScrolling = true
      } else {
        this.isScrolling = false
      }
      // Any code to be executed when the window is scrolled
    },
  },
   created() {
    if (process.browser) {
      if (window.scrollY > 0) {
        this.handleScroll()
      }
      window.addEventListener('scroll', this.handleScroll)
    }
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll)
  },
};
</script>
<style lang="scss">

</style>
