<template>
  <div class="bgImg">
    <div class="myLittleCard">
      <h3 class="textImportant">
        Dévelopeur Web Freelance
      </h3>
      <h3 class="textImportant">
        Thomas Jamais
      </h3>
      <a href="#presentation">
        <v-avatar color="#ebe9e8" class="myAvatar">
          <v-icon dark>
            mdi-chevron-triple-down
            <!-- mdi-account-circle -->
          </v-icon>
        </v-avatar>

      </a>
      <!-- <a href="#section04"><span></span>Scroll</a> -->
    </div>

    <!-- <img src="/background-hight.jpg" class="bgImg"> -->
  </div>
</template>

<style>
.myAvatar {
  border: 1px double white !important;
  margin-top: 10vh;
}

.bgImg {
  height: 100vh;
  width: 100vw;
  /* background-image: url('/background-hight.jpg');
  background-position: center;
  background-size: cover; */
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: #9c948d;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 1000'%3E%3Cg %3E%3Ccircle fill='%239c948d' cx='50' cy='0' r='50'/%3E%3Cg fill='%23a19992' %3E%3Ccircle cx='0' cy='50' r='50'/%3E%3Ccircle cx='100' cy='50' r='50'/%3E%3C/g%3E%3Ccircle fill='%23a69e98' cx='50' cy='100' r='50'/%3E%3Cg fill='%23aaa39d' %3E%3Ccircle cx='0' cy='150' r='50'/%3E%3Ccircle cx='100' cy='150' r='50'/%3E%3C/g%3E%3Ccircle fill='%23afa9a3' cx='50' cy='200' r='50'/%3E%3Cg fill='%23b4aea8' %3E%3Ccircle cx='0' cy='250' r='50'/%3E%3Ccircle cx='100' cy='250' r='50'/%3E%3C/g%3E%3Ccircle fill='%23b9b3ae' cx='50' cy='300' r='50'/%3E%3Cg fill='%23beb8b3' %3E%3Ccircle cx='0' cy='350' r='50'/%3E%3Ccircle cx='100' cy='350' r='50'/%3E%3C/g%3E%3Ccircle fill='%23c3bdb9' cx='50' cy='400' r='50'/%3E%3Cg fill='%23c8c3bf' %3E%3Ccircle cx='0' cy='450' r='50'/%3E%3Ccircle cx='100' cy='450' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ccc8c4' cx='50' cy='500' r='50'/%3E%3Cg fill='%23d1ceca' %3E%3Ccircle cx='0' cy='550' r='50'/%3E%3Ccircle cx='100' cy='550' r='50'/%3E%3C/g%3E%3Ccircle fill='%23d6d3d0' cx='50' cy='600' r='50'/%3E%3Cg fill='%23dbd8d6' %3E%3Ccircle cx='0' cy='650' r='50'/%3E%3Ccircle cx='100' cy='650' r='50'/%3E%3C/g%3E%3Ccircle fill='%23e0dedc' cx='50' cy='700' r='50'/%3E%3Cg fill='%23e5e3e1' %3E%3Ccircle cx='0' cy='750' r='50'/%3E%3Ccircle cx='100' cy='750' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ebe9e7' cx='50' cy='800' r='50'/%3E%3Cg fill='%23f0eeed' %3E%3Ccircle cx='0' cy='850' r='50'/%3E%3Ccircle cx='100' cy='850' r='50'/%3E%3C/g%3E%3Ccircle fill='%23f5f4f3' cx='50' cy='900' r='50'/%3E%3Cg fill='%23faf9f9' %3E%3Ccircle cx='0' cy='950' r='50'/%3E%3Ccircle cx='100' cy='950' r='50'/%3E%3C/g%3E%3Ccircle fill='%23ffffff' cx='50' cy='1000' r='50'/%3E%3C/g%3E%3C/svg%3E");
  background-attachment: fixed;
  background-size: contain;
  background-repeat-x: initial;
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

</style>
