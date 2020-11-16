<template>
  <v-app v-scroll="onScroll" light>
    <v-app-bar v-if="!fab" flat class="myBar">
      <v-toolbar-title class="myTitle cyan--text text--lighten-5" data-aos="zoom-in">
        Thomas Jamais
      </v-toolbar-title>
      <v-spacer />
      <!-- <v-icon>mdi-dots-vertical</v-icon> -->
      <span v-if="!isMobile" class="headerBtn" data-aos="fade-left" @click="navTo('##')">Présentation</span>
      <span
        v-if="!isMobile"
        class="headerBtn"
        data-aos="fade-left"
        data-aos-delay="600"
        @click="navTo('#technologies')"
      >
        Technologies
      </span>
      <span
        v-if="!isMobile"
        class="headerBtn"
        data-aos="fade-left"
        data-aos-delay="1200"
        @click="navTo('#experiences')"
      >
        Experiences
      </span>
      <span v-if="!isMobile" class="headerBtn" data-aos="fade-left" data-aos-delay="1800" @click="navTo('#projects')">Projects</span>
      <span v-if="!isMobile" class="headerBtn" data-aos="fade-left" data-aos-delay="2400" @click="navTo('#contact')">Contact</span>
    </v-app-bar>
    <v-main>
      <nuxt />
    </v-main>
    <v-btn
      v-show="fab"
      v-scroll="onScroll"
      class="upBtn"
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
    <v-btn
      v-show="fab"
      v-scroll="onScroll"
      class="downBtn"
      fab
      dark
      fixed
      bottom
      right
      color="#11270B"
      @click="toBottomOne"
    >
      <v-icon>keyboard_arrow_down</v-icon>
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
      fab: false,
      whereIm: 0,
      part: [0, '#presentation', '#technologies', '#experiences', '#projects', '#contact']
    }
  },
  mounted () {
    isMobile(this)
  },
  methods: {
    onScroll (e) {
      if (typeof window === 'undefined') { return }
      const top = window.pageYOffset || e.target.scrollTop || 0
      // console.log(window.pageYOffset, ', ', e.target.scrollTop)
      // console.log((window.pageYOffset / window.screen.availHeight).toFixed(0))
      this.whereIm = parseInt((window.pageYOffset / window.screen.availHeight).toFixed(0))
      this.fab = top > 20
    },
    toTop () {
      this.$vuetify.goTo(0)
      this.whereIm = 0
    },
    toBottomOne () {
      this.whereIm += 1
      // console.log('GOTO => ', this.whereIm, ', ', this.part[this.whereIm])
      this.$vuetify.goTo(this.part[this.whereIm])
    },
    navTo (to) {
      this.$vuetify.goTo(to)
    }
  }
}
</script>

<style>

.downBtn {
  bottom: 100px !important;
}

.upBtn {
  bottom: 176px ! important
}

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
  font-size: 2rem !important;
}

</style>
