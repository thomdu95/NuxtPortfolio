<template>
  <div class="container list-container">
    <h3 class="textImportant">
      Expériences
    </h3>
    <hr width="150px" class="myHr">
    <hr width="130px" class="myHr">
    <div id="experiences" class="main-timeline">
      <TimeElem v-for="(elem, id) in myLife" :key="elem.name" :elem="elem" :index="id" />
    </div>
  </div>
</template>

<script>

import TimeElem from './TimeElem'

export default {
  components: { TimeElem },
  data: () => ({
    myLife: [
      {
        month: '6 Mois',
        year: 2015,
        title: 'Développeur Web FullStack JS',
        company: 'Fizix.io',
        description: 'Dans une toute petite équipe (le CTO et moi même), nous avions la charge de développer et mettre en ligne les différentes plateformes Web (Front-Office et Back-Office) plus les différentes API et bases de données. En étroite collaboration avec le CTO de l\'époque j\'ai pu apprendre beaucoup et rapidement.',
        technos: [
          {
            name: 'ReactJS',
            color: '#222222',
            textColor: '#61DAFB'
          },
          {
            name: 'NodeJS',
            color: '#404137',
            textColor: '#83CD29'
          },
          {
            name: 'ExpressJS',
            color: '#F7DF1D',
            textColor: '#000100'
          }
        ]
      },
      {
        month: '4 Mois',
        year: 2016,
        title: 'Développeur Web',
        company: 'Les Ateliers du Val d\'oise',
        description: 'Première mission Freelance confiée par un ESAT. J\'avais en charge le maquetage ainsi que la réalisation complète puis la mise en production de leur site vitrine ayant pour but de présenter leur établissement. Le SEO a aussi été quelque chose à mettre en place pour se différencier des autres ESAT\'s.',
        technos: [
          {
            name: 'ES6',
            color: '#F7DF1D',
            textColor: '#000100'
          },
          {
            name: 'Bootstrap',
            color: '#7044A6',
            textColor: '#FFF'
          },
          {
            name: 'JQuery',
            color: '#144C9B',
            textColor: '#FFF'
          }
        ]
      },
      {
        month: '4 Mois',
        year: 2017,
        title: 'Développeur Web',
        company: 'Magic Folie\'s',
        description: 'Première site ecommerce confié par un professionnel de la magie qui avait pour ambition de vendre des différents tours de magie à ses clients. J\'avais en charge le maquetage ainsi que la réalisation complète du ecommerce. J\'ai d\'abord commencé par créer le site via VueJS , NodeJS et Express. Puis suis allé sur Prestashop.',
        technos: [
          {
            name: 'Prestashop',
            color: '#A4DBEA',
            textColor: '#DE006E'
          },
          {
            name: 'VueJS',
            color: '#31475E',
            textColor: '#3FB984'
          },
          {
            name: 'Vuex',
            color: '#31475E',
            textColor: '#3FB984'
          }
        ]
      },
      {
        month: '7 Mois',
        year: 2017,
        title: 'Formateur Developement Web',
        company: 'Coding Academy',
        description: 'Première expérience en tant que formateur au seins de la Coding Academy. Après une piscine de C, les projets portent sur le Dévelopement Web. La formation aborde plusieurs technologies différentes du Php au Js en passant par le Ruby. Les projets sont déjà fait, cependant je les mettais à jour et apportais mes corrections.',
        technos: [
          {
            name: 'AngularJS',
            color: '#C4002B',
            textColor: '#FFF'
          },
          {
            name: 'Symfony',
            color: '#000',
            textColor: '#FFF'
          },
          {
            name: 'JQuery',
            color: '#144C9B',
            textColor: '#FFF'
          },
          {
            name: 'RubyOnRails',
            color: '#CE0000',
            textColor: '#FFF'
          }
        ]
      },
      {
        month: '3 Mois',
        year: 2018,
        title: 'Developement Web',
        company: 'Saveur d\'Asie',
        description: 'Contrat bénévol pour aider une association française en Chine de vente de thé de qualité à bas prix. Après avoir commencé le site en VueJS égallement, j\'ai finis par choisir WP et WooCommerce pour pouvoir leur donner la main par la suite sans avoir à créer un Back Office spécial pour eux.',
        technos: [
          {
            name: 'VueJS',
            color: '#31475E',
            textColor: '#3FB984'
          },
          {
            name: 'WordPress',
            color: '#DBEFF7',
            textColor: '#453F3D'
          },
          {
            name: 'WooCommerce',
            color: '#7F54B3',
            textColor: '#FFF'
          }
        ]
      },
      {
        month: '2 Mois',
        year: 2018,
        title: 'Formateur Developement Web',
        company: 'Etna',
        description: 'Formateur au seins de l\'Etna. Présent pour la durée de leur piscine de C, PHP et Bash, les projets portent sur l\'algorithmie. Cette période est intensive, aussi bien pour les apprenants que pour les formateur. Les projets évoluent rapidement en difficultées.',
        technos: [
          {
            name: 'C',
            color: '#144C9B',
            textColor: '#FFF'
          },
          {
            name: 'Php',
            color: '#4F5B93',
            textColor: '#FFF'
          },
          {
            name: 'Bash',
            color: '#3C4549',
            textColor: '#FFF'
          }
        ]
      },
      {
        month: '1 Mois',
        year: 2018,
        title: 'Développeur Web FullStack JS',
        company: 'P3 Group',
        description: 'Petite mission de consultant JQuery et VueJS pour P3 Group. En 1 mois je suis intervenu sur 2 de leurs projets pour résoudre des problèmes techniques et des problèmes d\'implémentation. Bien que la mission n\'ai durée q\'un mois, j\'ai beaucoup aimé travaillé sur ces gros projets.',
        technos: [
          {
            name: 'JQuery',
            color: '#144C9B',
            textColor: '#FFF'
          },
          {
            name: 'VueJS',
            color: '#31475E',
            textColor: '#3FB984'
          },
          {
            name: 'NodeJS',
            color: '#404137',
            textColor: '#83CD29'
          }
        ]
      },
      {
        month: '2 x 7 Mois',
        year: 2019,
        title: 'Responsable Formateur Developement Web',
        company: 'Simplon.co',
        description: 'Responsable d\'une formation Dévelopeur Web et Web Mobile FullStack JS d\'une durée de 7 mois, je suis en charge d\'assurer leur monté en compétences à travers des projets (que je créer) ainsi que mon propre contenu pédagogique. La formation me permet de m\'ammeliorer à tous les points de vue.',
        technos: [
          {
            name: 'VueJS',
            color: '#31475E',
            textColor: '#3FB984'
          },
          {
            name: 'Vuex',
            color: '#31475E',
            textColor: '#3FB984'
          },
          {
            name: 'ReactJS',
            color: '#222222',
            textColor: '#61DAFB'
          },
          {
            name: 'Redux',
            color: '#7749BD',
            textColor: '#2C2C2C'
          },
          {
            name: 'NodeJS',
            color: '#404137',
            textColor: '#83CD29'
          },
          {
            name: 'ExpressJS',
            color: '#F7DF1D',
            textColor: '#000100'
          }
        ]
      }
    ]
  })
}
</script>

<style>
/* body{
    background-color: #f7f7f7;
    margin-top:20px;
} */

.myHr {
    margin-left: auto;
    margin-right: auto;
}

.main-timeline {
    position: relative;
    margin-top: 10vh;
}

.main-timeline:before {
  content: "";
  display: block;
  width: 2px;
  height: 100%;
  background: #c6c6c6;
  margin: 0 auto;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
}

.main-timeline .timeline {
  margin-bottom: 40px;
  position: relative;
}

.main-timeline .timeline:after {
  content: "";
  display: block;
  clear: both;
}

.main-timeline .icon {
  width: 18px;
  height: 18px;
  line-height: 18px;
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

.main-timeline .icon:before,
.main-timeline .icon:after {
  content: "";
  width: 100%;
  height: 100%;
  border-radius: 50%;
  position: absolute;
  top: 0;
  left: 0;
  transition: all 0.33s ease-out 0s;
}

.main-timeline .icon:before {
  background: #fff;
  border: 2px solid #232323;
  left: -3px;
}

.main-timeline .icon:after {
  border: 2px solid #c6c6c6;
  left: 3px;
}

.main-timeline .timeline:hover .icon:before {
  left: 3px;
}

.main-timeline .timeline:hover .icon:after {
  left: -3px;
}

.main-timeline .date-content {
  width: 50%;
  float: left;
  /* margin-top: 22px; */
  margin-top: 60px;
  position: relative;
}

.main-timeline .date-content:before {
  content: "";
  width: 36.5%;
  height: 2px;
  background: #c6c6c6;
  margin: auto 0;
  position: absolute;
  top: 0;
  right: 10px;
  bottom: 0;
}

.main-timeline .date-outer {
  width: 125px;
  height: 125px;
  font-size: 16px;
  text-align: center;
  margin: auto;
  z-index: 1;
}

.main-timeline .date-outer:before,
.main-timeline .date-outer:after {
  content: "";
  width: 125px;
  height: 125px;
  margin: 0 auto;
  border-radius: 50%;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  transition: all 0.33s ease-out 0s;
}

.main-timeline .date-outer:before {
  background: #fff;
  border: 2px solid #232323;
  left: -6px;
}

.main-timeline .date-outer:after {
  border: 2px solid #c6c6c6;
  left: 6px;
}

.main-timeline .timeline:hover .date-outer:before {
  left: 6px;
}

.main-timeline .timeline:hover .date-outer:after {
  left: -6px;
}

.main-timeline .date {
  width: 100%;
  margin: auto;
  position: absolute;
  top: 27%;
  left: 0;
}

.main-timeline .month {
  font-size: 18px;
  font-weight: 700;
}

.main-timeline .year {
  display: block;
  font-size: 30px;
  font-weight: 700;
  color: #232323;
  line-height: 36px;
}

.main-timeline .timeline-content {
  width: 50%;
  padding: 20px 0 20px 50px;
  float: right;
}

.main-timeline .title {
  font-size: 19px;
  font-weight: 700;
  line-height: 24px;
  margin: 0 0 15px 0;
}

.main-timeline .description {
  margin-bottom: 15px;
  /* margin */
}

.main-timeline .timeline:nth-child(2n) .date-content {
  float: right;
}

.main-timeline .timeline:nth-child(2n) .date-content:before {
  left: 10px;
}

.main-timeline .timeline:nth-child(2n) .timeline-content {
  padding: 20px 50px 20px 0;
  text-align: right;
}

@media only screen and (max-width: 991px) {
  .main-timeline .date-content {
    margin-top: 35px;
  }
  .main-timeline .date-content:before {
    width: 22.5%;
  }
  .main-timeline .timeline-content {
    padding: 10px 0 10px 30px;
  }
  .main-timeline .title {
    font-size: 17px;
  }
  .main-timeline .timeline:nth-child(2n) .timeline-content {
    padding: 10px 30px 10px 0;
  }
}

@media only screen and (max-width: 767px) {
  .main-timeline:before {
    margin: 0;
    left: 7px;
  }
  .main-timeline .timeline {
    margin-bottom: 20px;
  }
  .main-timeline .timeline:last-child {
    margin-bottom: 0;
  }
  .main-timeline .icon {
    margin: auto 0;
  }
  .main-timeline .date-content {
    width: 95%;
    float: right;
    margin-top: 0;
  }
  .main-timeline .date-content:before {
    display: none;
  }
  .main-timeline .date-outer {
    width: 110px;
    height: 110px;
  }
  .main-timeline .date-outer:before,
  .main-timeline .date-outer:after {
    width: 110px;
    height: 110px;
  }
  .main-timeline .date {
    top: 30%;
  }
  .main-timeline .year {
    font-size: 24px;
  }
  .main-timeline .timeline-content,
  .main-timeline .timeline:nth-child(2n) .timeline-content {
    width: 95%;
    text-align: center;
    padding: 10px 0;
  }
  .main-timeline .title {
    margin-bottom: 10px;
  }
}
</style>
