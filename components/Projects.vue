<template>
  <div id="projects" class="myProjects">
    <v-container class="myContainer technoContainer">
      <h3 class="textImportant" data-aos="zoom-in">
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
  .myProjects {
    background-color: #d3d1d1;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1600 900'%3E%3Cdefs%3E%3ClinearGradient id='a' x1='0' x2='0' y1='1' y2='0' gradientTransform='rotate(0,0.5,0.5)'%3E%3Cstop offset='0' stop-color='%230FF'/%3E%3Cstop offset='1' stop-color='%23CF6'/%3E%3C/linearGradient%3E%3ClinearGradient id='b' x1='0' x2='0' y1='0' y2='1' gradientTransform='rotate(0,0.5,0.5)'%3E%3Cstop offset='0' stop-color='%23F00'/%3E%3Cstop offset='1' stop-color='%23FC0'/%3E%3C/linearGradient%3E%3C/defs%3E%3Cg fill='%23FFF' fill-opacity='0' stroke-miterlimit='10'%3E%3Cg stroke='url(%23a)' stroke-width='4.949999999999999'%3E%3Cpath transform='translate(-81.9 3.5999999999999996) rotate(-1.8000000000000007 1409 581) scale(0.952084)' d='M1409 581 1450.35 511 1490 581z'/%3E%3Ccircle stroke-width='1.6500000000000001' transform='translate(-103.5 63) rotate(5.4 800 450) scale(1.004766)' cx='500' cy='100' r='40'/%3E%3Cpath transform='translate(13.5 -67.5) rotate(40.5 401 736) scale(1.004766)' d='M400.86 735.5h-83.73c0-23.12 18.74-41.87 41.87-41.87S400.86 712.38 400.86 735.5z'/%3E%3C/g%3E%3Cg stroke='url(%23b)' stroke-width='1.5'%3E%3Cpath transform='translate(378 1.799999999999999) rotate(-0.44999999999999973 150 345) scale(0.9900279999999999)' d='M149.8 345.2 118.4 389.8 149.8 434.4 181.2 389.8z'/%3E%3Crect stroke-width='3.3000000000000003' transform='translate(-103.5 -171) rotate(32.39999999999999 1089 759)' x='1039' y='709' width='100' height='100'/%3E%3Cpath transform='translate(-226.8 61.2) rotate(5.400000000000002 1400 132) scale(0.865)' d='M1426.8 132.4 1405.7 168.8 1363.7 168.8 1342.7 132.4 1363.7 96 1405.7 96z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    background-attachment: fixed;
    background-size: cover;
    border-top: 2px solid brown;
    border-bottom: 2px solid brown;
  }
</style>
