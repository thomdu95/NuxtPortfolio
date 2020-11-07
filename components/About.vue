<template>
  <div class="myContainer">
    <h3 id="presentation" class="textImportant">
      Présentation
    </h3>
    <hr width="150px">
    <hr width="130px">
    <p class="aboutPara">
      Dévelopeur Web depuis maintenant 5 ans et freelance depuis autant de temps, j'aime prendre en main des projets et leur donner vie !
      En plus de ça je suis aussi formateur en Dévelopement Web et Web mobile, j'adore être au contact de personnes désireuse d'apprendre.
      Amoureux de voyages et désieux de découvrir le maximum de cultures de mon vivant je suis aussi curieux que Pandore !
    </p>
    <img class="aboutPic" src="/thomasjamais.jpg">
    <div>
      <v-btn
        elevation="2"
        large
        outlined
      >
        <a href="https://www.linkedin.com/in/thomas-jamais-0968369a" target="_blank" class="textLink">Linkedin</a>
      </v-btn>
      <v-btn
        elevation="2"
        large
        outlined
      >
        <a href="https://hamacattitude.fr/" target="_blank">HamacAttitude</a>
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

.myContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 30vh 10vw;
    content-visibility: auto;
}

.aboutPara {
    width: 40vw;
    font-size: 1.5rem;
    font-weight: 300;
    margin-top: 5vh;
    text-align: center;
}

.aboutPic {
    margin-top: 5vh;
    margin-bottom: 5vh;
    border-radius: 50%;
    width: 400px;
}

hr {
    margin-bottom: 15px;
}

@media only screen and (max-width: 600px) {
  .aboutPara {
    width: unset;
  }
  .aboutPic {
    width: 250px;
  }
  .textLink {
    font-size: 0.8rem;
  }
}

</style>
