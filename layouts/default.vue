<template>
  <v-app v-scroll="onScroll" light>
    <v-app-bar v-if="!fab" flat class="myBar">
      <v-toolbar-title class="myTitle cyan--text text--lighten-5">
        Thomas Jamais
      </v-toolbar-title>
      <v-spacer />
      <!-- <v-icon>mdi-dots-vertical</v-icon> -->
      <span v-if="!isMobile" class="headerBtn" @click="navTo('#presentation')">Présentation</span>
      <span v-if="!isMobile" class="headerBtn" @click="navTo('#technologies')">Technologies</span>
      <span v-if="!isMobile" class="headerBtn" @click="navTo('#experiences')">Experiences</span>
      <span v-if="!isMobile" class="headerBtn" @click="navTo('#projects')">Projects</span>
      <span v-if="!isMobile" class="headerBtn" @click="navTo('#contact')">Contact</span>
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
  cursor: pointer;
  padding: 2px 5px;
  border-radius: 15%;
  color: #e0f7fa;
}

@keyframes btnHover {
  from {
    background-color: transparent;
    color: #e0f7fa;
  }
  to {
    background-color: #e0f7fa;
    color: black !important;
  }
}

.headerBtn:hover {
  animation: btnHover 200ms forwards;
}

html {
  scroll-behavior: smooth;
}

.myBar {
  top: 0px !important;
  position: fixed !important;
  background-color: transparent !important;
  z-index: 2 !important;
  border-bottom: 1px solid #E0F7FA !important;
  padding: 0 20vw;
}

.myTitle {
  color: #E0F7FA;
}

</style>
