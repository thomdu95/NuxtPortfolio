<template>
  <div id="technologies" class="languages" data-aos="zoom-in">
    <v-container class="myContainer technoContainer">
      <h3 class="textImportant">
        Mes Technologies
      </h3>
      <hr width="150px">
      <hr width="130px">
      <v-row style="margin-top: 5vh;">
        <v-col v-for="(l, nb) in languages" :key="l.name" cols="12" md="4">
          <Language :language="l" :nb="nb" />
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
    /* background-color: #eee; */
    background-color: #9c948d;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 1000'%3E%3Cg %3E%3Ccircle fill='%239c948d' cx='50' cy='0' r='50'/%3E%3Cg fill='%23a19992' %3E%3Ccircle cx='0' cy='50' r='50'/%3E%3Ccircle cx='100' cy='50' r='50'/%3E%3C/g%3E%3Ccircle fill='%23a69e98' cx='50' cy='100' r='50'/%3E%3Cg fill='%23aaa39d' %3E%3Ccircle cx='0' cy='150' r='50'/%3E%3Ccircle cx='100' cy='150' r='50'/%3E%3C/g%3E%3Ccircle fill='%23afa9a3' cx='50' cy='200' r='50'/%3E%3Cg fill='%23b4aea8' %3E%3Ccircle cx='0' cy='250' r='50'/%3E%3Ccircle cx='100' cy='250' r='50'/%3E%3C/g%3E%3Ccircle fill='%23b9b3ae' cx='50' cy='300' r='50'/%3E%3Cg fill='%23beb8b3' %3E%3Ccircle cx='0' cy='350' r='50'/%3E%3Ccircle cx='100' cy='350' r='50'/%3E%3C/g%3E%3Ccircle fill='%23c3bdb9' cx='50' cy='400' r='50'/%3E%3Cg fill='%23c8c3bf' %3E%3Ccircle cx='0' cy='450' r='50'/%3E%3Ccircle cx='100' cy='450' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ccc8c4' cx='50' cy='500' r='50'/%3E%3Cg fill='%23d1ceca' %3E%3Ccircle cx='0' cy='550' r='50'/%3E%3Ccircle cx='100' cy='550' r='50'/%3E%3C/g%3E%3Ccircle fill='%23d6d3d0' cx='50' cy='600' r='50'/%3E%3Cg fill='%23dbd8d6' %3E%3Ccircle cx='0' cy='650' r='50'/%3E%3Ccircle cx='100' cy='650' r='50'/%3E%3C/g%3E%3Ccircle fill='%23e0dedc' cx='50' cy='700' r='50'/%3E%3Cg fill='%23e5e3e1' %3E%3Ccircle cx='0' cy='750' r='50'/%3E%3Ccircle cx='100' cy='750' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ebe9e7' cx='50' cy='800' r='50'/%3E%3Cg fill='%23f0eeed' %3E%3Ccircle cx='0' cy='850' r='50'/%3E%3Ccircle cx='100' cy='850' r='50'/%3E%3C/g%3E%3Ccircle fill='%23f5f4f3' cx='50' cy='900' r='50'/%3E%3Cg fill='%23faf9f9' %3E%3Ccircle cx='0' cy='950' r='50'/%3E%3Ccircle cx='100' cy='950' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ffffff' cx='50' cy='1000' r='50'/%3E%3C/g%3E%3C/svg%3E");
    background-attachment: fixed;
    background-size: contain;
    background-repeat-x: initial;
}
</style>
