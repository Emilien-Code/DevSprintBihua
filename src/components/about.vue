<template>
  <div id="about">
    <img src="../assets/Accueil_a-propos.png" alt="">
    <div id="right">
      <div id="container">
        <h4>100% indépendante depuis 1973! </h4>
        <p>Expérience c’est avant tout une équipe, quatre libraires amoureux de la BD prêts à partager avec vous leurs plus belles lectures ! C’est aussi un lieu atypique où les plafonds sont recouverts de centaines de dédicaces.</p>
        <p>On allait oublier ! Expérience c’est aussi un atelier de sérigraphie où nous fabriquons nos propres productions.</p>
        <a id="test" href="/">
          En savoir plus
        </a>

      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'about',
}
</script>

<style scoped>
#about  {
  display: flex;
  background-color: #E85243;
}
img {
  width: 708px;
  height: 1024px;
  object-fit: cover;
}
a{
  color: #1D1D1D;
  font-size: 16px;
  background: #FADD4B;
  border-radius: 32px;
  padding: 12px 40px;

  font-style: normal;
  font-weight: 400;
  line-height: 28px;

  margin-top: 40px;
}
h4  {
  color: #FFFFFF;
  margin-bottom: 28px;
}
#right {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 1024px;
}

p{
  color: #FFFFFF;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 32px;
  margin-bottom: 16px;
}
#test {
  margin-top: 40px;
}
#container{
  width: 438px;
}

@media (max-width: 1385px) {
  #about{
    flex-direction: column-reverse;
    /*height: none;*/
  }
  #container{
    display: flex;
    flex-direction: column;
    justify-content: center ;
    align-items: center;
    width: 100%;
    background-color: #E85243;
    height: 534px;
    padding: 20px
  }
  a{
    width: 280px;
    text-align: center;
  }
  img{
    width: 100%;
  }
}

</style>
