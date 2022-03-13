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
      :class="isScrolling === true ? 'scrolled' : 'not-scrolled'"
      :clipped-left="clipped"
      fixed
      app
    >
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
      <Nuxt />
    </v-main>

    <v-footer>
      <Footer />
    </v-footer>
  </v-app>
</template>

<script>
import Footer from "@/components/core/Footer.vue";
export default {
  name: "DefaultLayout",
  components: {
    Footer,
  },
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
          to: "#header-section",
        },
        {
          icon: "mdi-apps",
          title: "Services",
          to: "#our-service-section",
        },
        {
          icon: "mdi-apps",
          title: "Work",
          to: "#recent-work-section",
        },
        {
          icon: "mdi-apps",
          title: "Blog",
          to: "#our-blog-section",
        },
        {
          icon: "mdi-apps",
          title: "Pricing",
          to: "#pricing-tables-section",
        },
        {
          icon: "mdi-apps",
          title: "Team",
          to: "#our-team-section",
        },
        {
          icon: "mdi-apps",
          title: "Contact",
          to: "#contanct-section",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
  methods: {
    handleScroll(event) {
      if (window.scrollY > 0) {
        this.isScrolling = true;
      } else {
        this.isScrolling = false;
      }
      // Any code to be executed when the window is scrolled
    },
  },
  created() {
    if (process.browser) {
      if (window.scrollY > 0) {
        this.handleScroll();
      }
      window.addEventListener("scroll", this.handleScroll);
    }
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>
<style lang="scss">
.scrolled {
  background: #2c2d31 !important;
}
.v-footer{
  padding: 0;
  // test
}
</style>

