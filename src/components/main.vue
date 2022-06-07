<template>
  <div id="main">
    <div :style="{transform: `translateY(${position*0.25}px)`}" id="img"></div>
    <h1  >LIBRAIRIE EXPÉRIENCE</h1>

    <span :style="{transform :`translateY(${-this.position/10 + 270}px)` }">100% indépendante</span>

    <span :style="{transform :`translateY(${-this.position/5 +500}px)` }">Depuis  1973</span>


    <div id="discover">
      <h4>Découvrez nos produits</h4>
      <p>
        Le plus grand choix d’affiches BD de la région, un large rayon
        Para BD approvisionné par la licence Moulinsart et la maison Tsume, et bien d’autres choses encore !
      </p>

      <a href="/">
        Accéder à la boutique
      </a>
    </div>

  </div>
</template>

<script>

export default {
  name: 'main',
  data: function () {
    return {
      position: 0
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll () {
      this.position = window.scrollY
    }
  }
}
</script>

<style scoped>
  h1  {
    position: absolute;
    z-index: 1;
    width: 606px;
    height: 228px;
    left: 155px;
    top: 475px;

    color: #1D1D1D;
  }
  #img{
    position: absolute;

    border-radius: 400px 400px 0 0;

    background: url(../assets/Accueil_premiere-img.png);
    background-repeat: no-repeat;
    background-size: cover;

    width: 784px;
    height: 1117px;
    left: 501px;
    top: 200px;
  }
  #main{
    background-color: #FFF5E6;
    width: 100vw;
    height: 2059px;
  }
  #discover{
    position: relative;
    top: 1550px;
    left: 50%;
    transform: translateX(-50%);
    width: 553px;
    text-align: center;
  }
  p{
    margin : 24px 0 40px 0
  }
  span{
    display: inline-block;
    position: relative;
    padding: 11px 20px;
    gap: 4px;
    z-index: 3;
    height: 41px;
    left: 25%;
    top: 250px;

    background: #5E5E5E;
    color: #FFFFFF;
    border-radius: 28px;
  }
  span:nth-child(1){
    left: calc(25%);
  }

  a{
    color: #1D1D1D;
    font-size: 16px;
    background: #FADD4B;
    border-radius: 32px;
    padding: 12px 40px;
    gap: 10px;
  }
  @media (max-width: 1385px) {
    #img{
      left:  25%;
    }

  }
</style>
