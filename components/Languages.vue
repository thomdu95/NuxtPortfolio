<template>
  <div class="languages">
    <v-container class="myContainer technoContainer">
      <h3 id="technologies" class="textImportant">
        Mes Technologies
      </h3>
      <hr width="150px">
      <hr width="130px">
      <v-row style="margin-top: 5vh;">
        <v-col v-for="l in languages" :key="l.name" cols="12" md="4">
          <Language :language="l" />
        </v-col>
      </v-row>
    </v-container>
  </div>
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
.technoContainer {
  width: 60vw !important;
  padding: unset;
}

.languages {
    background-color: #eee;
}
</style>
