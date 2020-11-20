<template>
  <div class="myContainer sectionPassionContainer">
    <h3 id="passions" class="textImportant">
      Mes Passions
    </h3>
    <hr width="150px">
    <hr width="130px" class="passionTitleEnd">
    <div class="passionsBigContainer">
      <Passion v-for="p in passions" :key="p.title" :passion="p" />
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    passions: [
      {
        title: 'RoadTrip',
        icon: 'mdi-earth',
        description: 'Voyager à travers la France, l\'Europe et le Monde fait vraiment parti de ma mentatilté. Un Hamac, un vélo et je suis parti pour explorer le monde.'
      },
      {
        title: 'Développer',
        icon: 'mdi-cellphone-link',
        description: 'Que ce soit pour moi ou pour mes proches, j\'adore développer et apprendre de nouvelles technologies. Je passe beaucoup de temps, quand l\'envie me prend, pour mener à bien mes projets.'
      },
      {
        title: 'Apprendre',
        icon: 'mdi-book-open-page-variant-outline',
        description: 'C\'est un fait, j\'aime apprendre de nouvelles choses, découvrir de nouveaux savoir, expérimenter de nouvelles expériences. Si l\'argent s\'échange contre du savoir, le savoir se suffit à lui même.'
      }
    ]
  })
}
</script>

<style>

.sectionPassionContainer {
    background-color: #F7F9FC;
    height: 50vh;
}

.passionsBigContainer {
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 100%;
}

.passionTitleEnd {
  margin-bottom: 10vh;
}

.passionContainer {
   width: 220px;
   height: 220px;
   display: -webkit-box;
   display: -ms-flexbox;
   display: flex;
   -webkit-box-pack: center;
       -ms-flex-pack: center;
           justify-content: center;
   -webkit-box-align: center;
       -ms-flex-align: center;
           align-items: center;
 }

 .mybox {
   position: absolute;
   width: 220px;
   height: 220px;
   display: -webkit-box;
   display: -ms-flexbox;
   display: flex;
   -webkit-box-pack: center;
       -ms-flex-pack: center;
           justify-content: center;
   -webkit-box-align: center;
       -ms-flex-align: center;
           align-items: center;
   -webkit-box-orient: vertical;
   -webkit-box-direction: normal;
       -ms-flex-direction: column;
           flex-direction: column;
   border-radius: 3px;
   overflow: hidden;
   -webkit-transition: -webkit-box-shadow ease 1s;
   transition: -webkit-box-shadow ease 1s;
   transition: box-shadow ease 1s;
   transition: box-shadow ease 1s, -webkit-box-shadow ease 1s;
 }

 .passionIcon {
   position: relative;
   margin-top: 8px;
   -webkit-transition: all 0.6s ease;
   transition: all 0.6s ease;
   -webkit-transition-delay: 0.32s;
           transition-delay: 0.32s;
   will-change: transform;
 }

 .icon_bg {
   width: 80px;
   height: 80px;
   border-radius: 100%;
   border: 1px solid rgba(225, 227, 232, 0.18);
   -webkit-box-shadow: 0 3px 4px 0 rgba(44, 71, 146, 0.25);
           box-shadow: 0 3px 4px 0 rgba(44, 71, 146, 0.25);
   background-color: #fff;
   display: -webkit-box;
   display: -ms-flexbox;
   display: flex;
   -webkit-box-pack: center;
       -ms-flex-pack: center;
           justify-content: center;
   -webkit-box-align: center;
       -ms-flex-align: center;
           align-items: center;
   -webkit-transition: all 0.6s ease;
   transition: all 0.6s ease;
   -webkit-transition-delay: 0.32s;
           transition-delay: 0.32s;
   will-change: transform;
 }

 .title {
   position: relative;
 }

 .super-box:hover .mybox {
 /*   border: 1px solid rgba(225, 227, 232, 0.18); */
   -webkit-box-shadow: 0 3px 4px 0 rgba(44, 71, 146, 0.25);
           box-shadow: 0 3px 4px 0 rgba(44, 71, 146, 0.25);
   -webkit-transition-delay: 0.32s;
           transition-delay: 0.32s;
 }

 .super-box:hover .icon_bg {
   -webkit-transform: translateY(-32px) scale(6);
           transform: translateY(-32px) scale(6);
 }

 .super-box:hover .passionIcon {
     /* 48 */
   -webkit-transform: translateY(-90px) scale(1.4);
           transform: translateY(-90px) scale(1.4);
 }

.super-box {
     width: 220px;
   height: 220px;
   display: -webkit-box;
   display: -ms-flexbox;
   display: flex;
   -webkit-box-pack: center;
       -ms-flex-pack: center;
           justify-content: center;
   -webkit-box-align: center;
       -ms-flex-align: center;
           align-items: center;
   -webkit-box-orient: vertical;
   -webkit-box-direction: normal;
       -ms-flex-direction: column;
           flex-direction: column;
 }

 .text {
   position: relative;
   top: -32px;
   width: 200px;
   text-align: center;
   -webkit-transition: all 0.4s ease;
   transition: all 0.4s ease;
   -webkit-transition-delay: 0.32s;
           transition-delay: 0.32s;
 }

 .super-box:hover .text {
   opacity: 0;
   -webkit-transform: translateY(-4px) scale(.8);
           transform: translateY(-4px) scale(.8);
 }

 .mybox::after {
   position: absolute;
   width: 170px;
   opacity: 0;
   font-size: 13px;
   color: #5d6494;
   line-height: 20px;
   -webkit-transition: all 0.3s ease;
   transition: all 0.3s ease;
   -webkit-transition-delay: 0.32s;
           transition-delay: 0.32s;
 }

 .super-box:hover .mybox::after {
   opacity: 1;
 }

.dr {
position: absolute;
  bottom: 16px;
  right: 16px;
  width:100px;
}

@media only screen and (min-width: 600px) {
  .sectionPassionContainer {
    min-height: 500px;
  }
}

@media only screen and (max-width: 600px) {
  .sectionPassionContainer {
    height: 120vh;
  }

  .passionsBigContainer {
    flex-direction: column;
  }
}

</style>
