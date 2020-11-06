<template>
  <v-app light>
    <v-app-bar dense>
      <v-btn href="#presentation" class="headerBtn">
        Présentation
      </v-btn>
      <v-btn href="#technologies" class="headerBtn">
        Technologies
      </v-btn>
    </v-app-bar>
    <v-main>
      <nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Thomas Jamais'
    }
  }
}
</script>

<style>
.headerBtn {
  margin-left: 2vw;
}
</style>
