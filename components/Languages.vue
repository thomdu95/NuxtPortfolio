<template>
  <v-container class="pa-4">
    <h3 id="technologies" class="textImportant">
      Mes Technologies
    </h3>
    <v-row>
      <v-col v-for="l in languages" :key="l.name" cols="12" md="4">
        <Language :language="l" />
      </v-col>
    </v-row>
    <p>lol</p>
  </v-container>
</template>

<script>
import Language from '~/components/Language'
export default {
  components: { Language },
  data () {
    return {
      languages: [
        {
          name: 'VueJS',
          img: '/vuelogo.svg',
          years: '4'
        },
        {
          name: 'ReactJs',
          img: '/reactlogo.png',
          years: '6'
        },
        {
          name: 'NodeJS',
          img: '/nodelogo.png',
          years: '6'
        },
        {
          name: 'Nuxt',
          img: '/nuxtlogo.png',
          years: '2'
        }
      ]
    }
  }
}
</script>

<style>
</style>
