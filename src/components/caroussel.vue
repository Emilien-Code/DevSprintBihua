<template>
  <div id="caroussel">
    <div id="container" :style="{transform: `translateX(${positionX}px)`, transitionDuration : `${duration}s`}">

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/10-ANS-DE-LA-GOUTTIERE-1.png" alt="">
        </div>
        <div class="bottom">
          <span>10 ANS DE LA GOUTTIÈRE</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/Après-le-bain-1.png" alt="">
        </div>
        <div class="bottom">
          <span>APRÈS LE BAIN...</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/AU-PIC-1.png" alt="">
        </div>
        <div class="bottom">
          <span>LA DANSE</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/BANDIT1.png" alt="">
        </div>
        <div class="bottom">
          <span>BANDIT</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/Couchédesoleil1.png" alt="">
        </div>
        <div class="bottom">
          <span>COUCHÉ DU SOLEIL</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/10-ANS-DE-LA-GOUTTIERE-1.png" alt="">
        </div>
        <div class="bottom">
          <span>10 ANS DE LA GOUTTIÈRE</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/Après-le-bain-1.png" alt="">
        </div>
        <div class="bottom">
          <span>APRÈS LE BAIN...</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/AU-PIC-1.png" alt="">
        </div>
        <div class="bottom">
          <span>LA DANSE</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/BANDIT1.png" alt="">
        </div>
        <div class="bottom">
          <span>BANDIT</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/Couchédesoleil1.png" alt="">
        </div>
        <div class="bottom">
          <span>COUCHÉ DU SOLEIL</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/10-ANS-DE-LA-GOUTTIERE-1.png" alt="">
        </div>
        <div class="bottom">
          <span>10 ANS DE LA GOUTTIÈRE</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/Après-le-bain-1.png" alt="">
        </div>
        <div class="bottom">
          <span>APRÈS LE BAIN...</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/AU-PIC-1.png" alt="">
        </div>
        <div class="bottom">
          <span>LA DANSE</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/BANDIT1.png" alt="">
        </div>
        <div class="bottom">
          <span>BANDIT</span><span>19,99€</span>
        </div>
      </div>

      <div class="article">
        <div class="top">
          <img src="../assets/caroussel/Couchédesoleil1.png" alt="">
        </div>
        <div class="bottom">
          <span>COUCHÉ DU SOLEIL</span><span>19,99€</span>
        </div>
      </div>


    </div>

      <div id="buttons">

        <button @click="previous">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M8 16L9.41 14.59L3.83 9L16 9L16 7L3.83 7L9.42 1.42L8 -3.49691e-07L-3.49691e-07 8L8 16Z" fill="#FFF5E5"/>
          </svg>
        </button>
        <button @click="next">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M8 16L9.41 14.59L3.83 9L16 9L16 7L3.83 7L9.42 1.42L8 -3.49691e-07L-3.49691e-07 8L8 16Z" fill="#FFF5E5"/>
          </svg>
        </button>

      </div>

  </div>
</template>

<script>

export default {
  name: 'caroussels',
  data: function () {
    return {
      positionX: 0,
      count: 1,
      duration : 0.5
    }
  },
  methods: {
    previous(){
      this.duration = 0.5;
      if(this.count > 1){
        this.positionX += 322+24;
        this.count--;
      }
    },
    next(){
      this.duration = 0.5;

      if (this.count == 6){
        this.count = 0;
        this.duration = 0;
      }

      this.positionX = -this.count * (322+24);
      this.count++;


      console.log(this.count)
    }
  }
}
</script>

<style scoped>
#caroussel{
  background-color: #FFF5E6;
  height: 687px;
  overflow: hidden;
}
  #container{
    display: flex;
    height: 447px;
    width: 10000000px;
    transition: .5s ease-out;
  }
  .article{
    cursor: pointer;
    margin-left: 24px;
    width: 322px;
    height: 403px;
  }
  .top  {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    background-color: #FFFFFF;
    height: 332px;
  }
  .bottom {
    padding-top: 12px;
    font-size: 20px;
    display: flex;
    justify-content: space-between;
  }
  Button{
    background-color: #1D1D1D;
    border: none;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    cursor: pointer;
    margin-right: 12px;
  }
  Button:nth-child(2){
    transform: rotateZ(180deg);
  }

  #buttons{
    position: absolute;
    right: 115px;
  }


</style>
