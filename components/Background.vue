<template>
  <div class="bgImg">
    <div class="newCard" data-aos="flip-left" data-aos-delay="1200">
      <h3 class="textImportant cyan--text text--lighten-5">
        Dévelopeur Web Freelance.
      </h3>
      <p class="cyan--text text--lighten-5">
        Dévelopeur depuis maintenant 7 ans, je me suis tourné vers le Web depuis 5 ans environ, en même temps que mes études. Découvrez ici une galerie de certains de mes projets perso. Vous pouvez aussi me contacter. A très vite et bonne visite.
      </p>
      <v-btn
        class="myAvatar"
        fab
        outlined
        color="white"
        data-aos="zoom-in"
        data-aos-delay="1800"
        @click="todown"
      >
        <v-icon>mdi-chevron-triple-down</v-icon>
      </v-btn>
    </div>
    <!-- <div class="myLittleCard">
      <h3 class="textImportant">
        Dévelopeur Web Freelance
      </h3>
      <h3 class="textImportant">
        Thomas Jamais
      </h3>
      <v-btn
        class="myAvatar"
        fab
        outlined
        color="white"
        @click="todown"
      >
        <v-icon>mdi-chevron-triple-down</v-icon>
      </v-btn>
    </div> -->
  </div>
</template>

<script>
export default {
  methods: {
    todown () {
      this.$vuetify.goTo('#presentation')
    }
  }
}
</script>
<style>

.myLink {
  text-decoration: none;
}

.myAvatar {
  /* margin-top: 10vh; */
  left: 40%
}

.newCard {
  padding-top: 30vh;
  margin-left: 15vw;
  width: 30vw;
}

.bgImg {
  height: 100vh;
  width: 100vw;
  /* background-image: url('/background-hight.jpg');
  background-position: center;
  background-size: cover; */
  /* display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: #9c948d; */
  background-image: url('/bg-stones.jpg');
  /* background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 1000'%3E%3Cg %3E%3Ccircle fill='%239c948d' cx='50' cy='0' r='50'/%3E%3Cg fill='%23a19992' %3E%3Ccircle cx='0' cy='50' r='50'/%3E%3Ccircle cx='100' cy='50' r='50'/%3E%3C/g%3E%3Ccircle fill='%23a69e98' cx='50' cy='100' r='50'/%3E%3Cg fill='%23aaa39d' %3E%3Ccircle cx='0' cy='150' r='50'/%3E%3Ccircle cx='100' cy='150' r='50'/%3E%3C/g%3E%3Ccircle fill='%23afa9a3' cx='50' cy='200' r='50'/%3E%3Cg fill='%23b4aea8' %3E%3Ccircle cx='0' cy='250' r='50'/%3E%3Ccircle cx='100' cy='250' r='50'/%3E%3C/g%3E%3Ccircle fill='%23b9b3ae' cx='50' cy='300' r='50'/%3E%3Cg fill='%23beb8b3' %3E%3Ccircle cx='0' cy='350' r='50'/%3E%3Ccircle cx='100' cy='350' r='50'/%3E%3C/g%3E%3Ccircle fill='%23c3bdb9' cx='50' cy='400' r='50'/%3E%3Cg fill='%23c8c3bf' %3E%3Ccircle cx='0' cy='450' r='50'/%3E%3Ccircle cx='100' cy='450' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ccc8c4' cx='50' cy='500' r='50'/%3E%3Cg fill='%23d1ceca' %3E%3Ccircle cx='0' cy='550' r='50'/%3E%3Ccircle cx='100' cy='550' r='50'/%3E%3C/g%3E%3Ccircle fill='%23d6d3d0' cx='50' cy='600' r='50'/%3E%3Cg fill='%23dbd8d6' %3E%3Ccircle cx='0' cy='650' r='50'/%3E%3Ccircle cx='100' cy='650' r='50'/%3E%3C/g%3E%3Ccircle fill='%23e0dedc' cx='50' cy='700' r='50'/%3E%3Cg fill='%23e5e3e1' %3E%3Ccircle cx='0' cy='750' r='50'/%3E%3Ccircle cx='100' cy='750' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ebe9e7' cx='50' cy='800' r='50'/%3E%3Cg fill='%23f0eeed' %3E%3Ccircle cx='0' cy='850' r='50'/%3E%3Ccircle cx='100' cy='850' r='50'/%3E%3C/g%3E%3Ccircle fill='%23f5f4f3' cx='50' cy='900' r='50'/%3E%3Cg fill='%23faf9f9' %3E%3Ccircle cx='0' cy='950' r='50'/%3E%3Ccircle cx='100' cy='950' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ffffff' cx='50' cy='1000' r='50'/%3E%3C/g%3E%3C/svg%3E");
  background-attachment: fixed;
  background-size: contain;
  background-repeat-x: initial; */
}

.myLittleCard {
    background-color: #ffffff6e;
    padding: 5vh;
      display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.textImportant {
    font-weight: 400;
    font-size: 3rem;
    color: #11270B;
    text-align: center;
}

.newCard > .textImportant {
      font-size: 2.7em;
    letter-spacing: 1px;
}

.newCard > p {
  text-align: justify;
  font-size: 0.9em;
  line-height: 2em;
}

.myLittleCard a {
  padding-top: 60px;
}
.myLittleCard a span {
  position: absolute;
  top: 0;
  left: 50%;
  width: 46px;
  height: 46px;
  margin-left: -23px;
  border: 1px solid #fff;
  border-radius: 100%;
  box-sizing: border-box;
}
.myLittleCard a span::after {
  position: absolute;
  top: 50%;
  left: 50%;
  content: '';
  width: 16px;
  height: 16px;
  margin: -12px 0 0 -8px;
  border-left: 1px solid #fff;
  border-bottom: 1px solid #fff;
  -webkit-transform: rotate(-45deg);
  transform: rotate(-45deg);
  box-sizing: border-box;
}
.myLittleCard a span::before {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  content: '';
  width: 44px;
  height: 44px;
  box-shadow: 0 0 0 0 rgba(255,255,255,.1);
  border-radius: 100%;
  opacity: 0;
  -webkit-animation: sdb03 3s 5;
  animation: sdb03 3s 5;
  box-sizing: border-box;
}
@-webkit-keyframes sdb03 {
  0% {
    opacity: 0;
  }
  30% {
    opacity: 1;
  }
  60% {
    box-shadow: 0 0 0 60px rgba(255,255,255,.1);
    opacity: 0;
  }
  100% {
    opacity: 0;
  }
}
@keyframes sdb03 {
  0% {
    opacity: 0;
  }
  30% {
    opacity: 1;
  }
  60% {
    box-shadow: 0 0 0 60px rgba(255,255,255,.1);
    opacity: 0;
  }
  100% {
    opacity: 0;
  }
}

@media only screen and (max-width: 600px) {
  .bgImg {
    background-size: cover;
  }

  .newCard > p {
    width: 90vw;
    margin: auto;
    margin-top: 2vh
  }

  .newCard {
    margin-left: unset;
    width: unset;
  }
}

</style>
