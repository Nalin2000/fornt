<template>
  <v-app dark>
    <v-card>
      <v-card-title class="nav text-center justify-center py-6"
        ><h1 class="font-weight-bold display-3 basil--text">
          LYNN Hotel
        </h1></v-card-title
      >
      <v-tabs background-color="nav" color="basil" grow>
        <v-tab
          v-for="(item, i) in items"
          :key="i"
          class="nav"
          :to="item.to"
          router
          exact
        >
          {{ item.title }}
        </v-tab>
      </v-tabs>
    </v-card>
    <v-btn
      v-show="fab"
      v-scroll="onScroll"
      fab
      dark
      fixed
      bottom
      right
      class="mb-6"
      color="btn"
      @click="toTop"
    >
      <v-icon size="50">mdi-menu-up</v-icon>
    </v-btn>

    <v-main class="main">
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer class="nav" :absolute="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: true,
      fixed: false,
      fab: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Room',
          to: '/#room',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Facilitate',
          to: '/#Facilitate',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Gallary',
          to: '/#gallary',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Contact',
          to: '/#contact',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 20
    },
    toTop() {
      this.$vuetify.goTo(0)
    },
  },
}
</script>
