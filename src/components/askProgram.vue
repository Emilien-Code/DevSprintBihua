<template>
  <div id="program">

    <h3>Demandez le programme</h3>
    <p>À la librairie, on adore faire rencontrer lecteurs et auteurs. Entre dédicaces, festivals, soirées à l’atelier de sérigraphies… nos événements sont nombreux et réguliers</p>



    <a href="/">
      Tous nos événements
    </a>

    <div id="programContainer">
      <div class="book">
        <div class="top">
          <img src="../assets/image1.png" alt="">
        </div>
        <div class="bottom">
          <h4>Priscilla et les enfants d'abord !</h4>
        </div>
          <span class="date">
            01/01/2022
          </span>
      </div >

      <div class="book">
        <div class="top">
          <img src="../assets/image1.png" alt="">
        </div>
        <div class="bottom">
          <h4>Priscilla et les enfants d'abord !</h4>
        </div>
        <span class="date">
            01/01/2022
          </span>
      </div >

      <div class="book">
        <div class="top">
          <img src="../assets/image1.png" alt="">
        </div>
        <div class="bottom">
          <h4>Priscilla et les enfants d'abord !</h4>
        </div>
        <span class="date">
            01/01/2022
          </span>
      </div >


    </div>


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
#program {
  height:1315px;
  background-color: #FFF5E5;
  justify-content: center ;
  display: flex;
  flex-direction: column;
  align-items: center;

}

p{
  margin-top: 24px;
  width: 553px;
  height: 96px;
  text-align:center;
}
a{
  color:  #1D1D1D;
  font-size: 16px;
  background: #FADD4B;
  border-radius: 32px;
  padding: 12px 40px;

  font-style: normal;
  font-weight: 400;
  line-height: 28px;

  margin: 40px 0 80px 0;
}

#programContainer{
  display: flex;
  justify-content: space-around;
  width: 1044px;
}

.top{
  width: 322px;
  height: 404px;
  background: #FFFFFF;
  display: flex;
  justify-content: center;
  align-items: center;
}
h4  {
  margin-top: 16px;
  width: 224px;
  text-align: center;
}
span{
  margin-top: 4px;
  text-align: center;
}
.book {
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>
