<template>
  <v-app light>
    <v-app-bar dense>
      <v-btn href="#presentation">
        Présentation
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
