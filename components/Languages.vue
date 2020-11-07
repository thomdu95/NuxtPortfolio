<template>
  <div id="technologies" class="languages">
    <v-container class="myContainer technoContainer">
      <h3 class="textImportant">
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
          years: '4',
          star: 5,
          description: 'J\'ai découvert VueJS en recevant un mail de JS weekly qui annonçait la V2 de VueJs (que je ne connaissait pas à l\'époque). J\'ai tout de suite ouvert VS Code et me suis mis à coder mon premier site avec VueJS (il s\'agissait de récupérer tous les pays du monde via une API et les afficher sous forme de card.'
        },
        {
          name: 'ReactJs',
          img: '/reactlogo.png',
          years: '6',
          star: 4,
          description: 'J\'ai découvert ReactJS très peu de temps après sa mise en BSD en avril 2015, lors de mon tout premier stage en dévelopement Web. J\'avais à l\'époque 19 ans et me suis émerveillé sur la manière de déveloper via des composants, avec des cycles de vie etc. J\'ai appris le dévelopement web via ReactJs finalement et en suis très fier. '
        },
        {
          name: 'NodeJS',
          img: '/nodelogo.png',
          years: '6',
          star: 4,
          description: 'De la même manière que j\'ai découvert ReactJS lors de mon premier stage en dévelopement web en 2015 à 19ans, j\'ai découvert NodeJS en même temps. En effet, lors de la mise en place de l\'application Web en React nous avons du faire tourné un serveur NodeJS. De plus nous avions crée une API via Express, MongoDb, BCrypt etc. Depuis, je réalise tous mes projets avec serveur Node.'
        },
        {
          name: 'Nuxt',
          img: '/nuxtlogo.png',
          years: '2',
          star: 5,
          description: 'Pour ce qui est de Nuxt, je l\'ai découvert de la même manière que VueJS, en lisant mes mails (vue weekly). Etant déjà formateur dans le dévelopement Web j\'ai tout de suite tenu à l\'essayer pour voir si j\'allais devoir abordé ce framework avec mes apprenants ou non. Le fait est que j\'ai adoré Nuxt pour ça rapidité, son optimisation ainsi que pour sa simplicité, cependnat j\'ai fais le choix d\'aborder d\'abord VueJS avant Nuxt pour avoir toutes les bases en main.'
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
  content-visibility: auto;
}

@media only screen and (max-width: 600px) {
  .technoContainer {
    width: unset !important;
  }
}

.languages {
    background-color: #eee;
}
</style>
