<template>
  <v-app light>
    <v-app-bar dense>
      <v-toolbar-title>Thomas Jamais</v-toolbar-title>
      <v-spacer />
      <!-- <v-icon>mdi-dots-vertical</v-icon> -->
      <v-btn v-if="!isMobile" href="#presentation" class="headerBtn">
        Présentation
      </v-btn>
      <v-btn v-if="!isMobile" href="#technologies" class="headerBtn">
        Technologies
      </v-btn>
    </v-app-bar>
    <v-main>
      <nuxt />
    </v-main>
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
      isMobile: false
    }
  },
  mounted () {
    isMobile(this)
  }
}
</script>

<style>
.headerBtn {
  margin-left: 2vw;
}
</style>
