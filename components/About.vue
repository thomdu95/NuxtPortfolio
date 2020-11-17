<template>
  <div class="myContainer about">
    <h3 id="presentation" class="textImportant">
      Présentation
    </h3>
    <hr width="150px">
    <hr width="130px">
    <div class="aboutRow">
      <div>
        <p class="aboutPara">
          Dévelopeur Web depuis maintenant 5 années et freelance depuis autant de temps, j'aime prendre en main des projets et leur donner vie !
          En plus de ça je suis aussi formateur en Dévelopement Web et Web mobile, j'adore être au contact de personnes désireuses d'apprendre.
          Amoureux de voyages et voulant découvrir le maximum de cultures, je suis aussi curieux que Pandore, ma curiosité est insatiable !
        </p>
      </div>
      <div class="picContainer">
        <img class="aboutPic lazyload" data-src="/thomasjamais.jpg">
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
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

.about {
  background-color: #F7F9FC;
}

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
    font-size: 1.2rem;
  }
  .aboutPic {
    width: 250px;
  }
  .textLink {
    font-size: 0.8rem;
  }

  .picContainer {
    text-align: center;
  }

  .myContainer {
    padding: 10vh 10vw;
  }
}

@media only screen and (min-width: 600px) {
  .aboutRow {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 75vw;
}
}

</style>
