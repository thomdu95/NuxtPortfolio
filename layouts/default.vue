<template>
  <v-app v-scroll="onScroll" light>
    <v-app-bar dense>
      <v-toolbar-title>Thomas Jamais</v-toolbar-title>
      <v-spacer />
      <!-- <v-icon>mdi-dots-vertical</v-icon> -->
      <v-btn v-if="!isMobile" class="headerBtn" @click="navTo('#presentation')">
        Présentation
      </v-btn>
      <v-btn v-if="!isMobile" class="headerBtn" @click="navTo('#technologies')">
        Technologies
      </v-btn>
      <v-btn v-if="!isMobile" class="headerBtn" @click="navTo('#experiences')">
        Experiences
      </v-btn>
      <v-btn v-if="!isMobile" class="headerBtn" @click="navTo('#projects')">
        Projects
      </v-btn>
    </v-app-bar>
    <v-main>
      <nuxt />
    </v-main>
    <v-btn
      v-show="fab"
      v-scroll="onScroll"
      fab
      dark
      fixed
      bottom
      right
      color="#11270B"
      @click="toTop"
    >
      <v-icon>keyboard_arrow_up</v-icon>
    </v-btn>
  </v-app>
</template>

<script>

import isMobile from '~/middleware/isMobile'

export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Thomas Jamais',
      isMobile: false,
      fab: false
    }
  },
  mounted () {
    isMobile(this)
  },
  methods: {
    onScroll (e) {
      if (typeof window === 'undefined') { return }
      const top = window.pageYOffset || e.target.scrollTop || 0
      // console.log(top)
      this.fab = top > 20
    },
    toTop () {
      this.$vuetify.goTo(0)
    },
    navTo (to) {
      this.$vuetify.goTo(to)
    }
  }
}
</script>

<style>
.headerBtn {
  margin-left: 2vw;
}

html {
  scroll-behavior: smooth;
}
</style>
