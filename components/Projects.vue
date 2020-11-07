<template>
  <div id="projects" class="myProjects" data-aos="zoom-in">
    <v-container class="myContainer technoContainer">
      <h3 class="textImportant">
        Certains projets
      </h3>
      <hr width="150px">
      <hr width="130px">
      <v-row style="margin-top: 5vh;">
        <v-col v-for="p in projects" :key="p.name" cols="12" md="4">
          <Project :project="p" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Project from '~/components/Project'
export default {
  components: { Project },
  data () {
    return {
      projects: [
        {
          name: 'Country',
          img: '/siteReact.jpg',
          link: 'http://www.country.thomas-jamais.fr/',
          star: 5,
          shortDes: 'Trier les pays et jouer avec',
          description: 'Projet fait en ReactJS et ReactBootstrap. C\'est un mini projet qui à pour but de démontrer certaines des mes compétences dans le dévelopement sous React. Il n\'y a pas Redux pour celui là et il est entierement fait avec des Hooks. Il est biensur à l\'état embriyonaire mais il reste décent et permet de justifier quelques compétences.\nIl a été créée en 5heures.'
        },
        {
          name: 'Country2',
          img: '/siteReact.jpg',
          link: 'http://www.country.thomas-jamais.fr/',
          star: 5,
          shortDes: 'Trier les pays et jouer avec',
          description: 'Projet fait en ReactJS et ReactBootstrap. C\'est un mini projet qui à pour but de démontrer certaines des mes compétences dans le dévelopement sous React. Il n\'y a pas Redux pour celui là et il est entierement fait avec des Hooks. Il est biensur à l\'état embriyonaire mais il reste décent et permet de justifier quelques compétences.\nIl a été créée en 5heures.'
        },
        {
          name: 'Country3',
          img: '/siteReact.jpg',
          link: 'http://www.country.thomas-jamais.fr/',
          star: 5,
          shortDes: 'Trier les pays et jouer avec',
          description: 'Projet fait en ReactJS et ReactBootstrap. C\'est un mini projet qui à pour but de démontrer certaines des mes compétences dans le dévelopement sous React. Il n\'y a pas Redux pour celui là et il est entierement fait avec des Hooks. Il est biensur à l\'état embriyonaire mais il reste décent et permet de justifier quelques compétences.\nIl a été créée en 5heures.'
        }
      ]
    }
  }
}</script>

<style>

</style>
