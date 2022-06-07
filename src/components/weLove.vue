<template>
  <div id="love">
    <div id="container  ">
    <h1>ON ADORE !</h1>

      <span :style="{transform :`translateY(${-this.p/10 + 300}px)` }">Notre dernier coup de coeur</span>

      <div id="imgctner" :style="{transform :`translate(-50%, ${-this.p/25 + 100}px) rotate(${this.p/100 - 20}deg)`}">
        <div id="img" :style="{transform :`translate( ${xp/5 - 200}px , ${yp/5  - 200}px) rotate(${xp/100}deg)`}"></div>
      </div>
    </div>
    <p>On vous aide à y voir plus clair parmi toutes ces sorties BD.</p>
  <a href="/">
    Découvrir nos coups de coeur
  </a>
  </div>



</template>

<script>
export default {
  name: 'about',
  data: function () {
    return {

      p:0
    }
  },
  created () {
    window.addEventListener('scroll', this.scrollH);
  },
  methods: {
    scrollH(){
      this.p = window.scrollY;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#love {
  height:1315px;
  background-color: #FADD4B;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

}
#img {
  position: relative;
  z-index: 2;

  top: 50%;
  left: 50%;

  transform: translate(-50%, -50%);

  height:  366px;
  width: 260px;

  background: url(../assets/BLACK-HAMMER1.png);
  background-repeat: no-repeat;
  background-size: cover;
}
#imgctner{
  position: relative;
  z-index: 1;
  left: 50%;
  transform: translate(-50%, -100px) rotate(5deg);
  border: solid black 1px;
  width: 400px;
  height: 500px;
  background-color: #FADD4B;
}
p{
  margin-top: 130px;
}
a{
  color:  #FFFFFF;
  font-size: 16px;
  background: #1D1D1D;
  border-radius: 32px;
  padding: 12px 40px;

  font-style: normal;
  font-weight: 400;
  line-height: 28px;

  margin-top: 40px;
}
span{
  display: inline-block;
  position: relative;
  padding: 11px 20px;
  gap: 4px;
  z-index: 3;
  height: 41px;
  left: 60%;
  top: 250px;

  background: #5E5E5E;
  color: #FFFFFF;
  border-radius: 28px;}
</style>
