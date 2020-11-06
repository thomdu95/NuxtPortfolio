<template>
  <div class="bgImg">
    <div class="myLittleCard">
      <h3 class="textImportant">
        Dévelopeur Web Freelance
      </h3>
      <h3 class="textImportant">
        Thomas Jamais
      </h3>
    </div>

    <!-- <img src="/background-hight.jpg" class="bgImg"> -->
  </div>
</template>

<style>
.bgImg {
  height: 100vh;
  width: 100vw;
  background-image: url('/background-hight.jpg');
  background-position: center;
  background-size: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
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
}
</style>
