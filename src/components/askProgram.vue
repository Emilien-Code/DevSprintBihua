<template>
  <div id="program">

    <h3>Demandez le programme</h3>
    <p>À la librairie, on adore faire rencontrer lecteurs et auteurs. Entre dédicaces, festivals, soirées à l’atelier de sérigraphies… nos événements sont nombreux et réguliers</p>



    <a href="/">
      Tous nos événements
    </a>

    <div id="programContainer" :style="{transform: `translateX(${positionX}px)`}" >
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
    <div id="buttons">

      <button @click="previous" :class="{notClickable: count==1}">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M8 16L9.41 14.59L3.83 9L16 9L16 7L3.83 7L9.42 1.42L8 -3.49691e-07L-3.49691e-07 8L8 16Z" fill="#FFF5E5"/>
        </svg>
      </button>
      <button @click="next" :class="{notClickable: count==3}">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M8 16L9.41 14.59L3.83 9L16 9L16 7L3.83 7L9.42 1.42L8 -3.49691e-07L-3.49691e-07 8L8 16Z" fill="#FFF5E5"/>
        </svg>
      </button>

    </div>


    </div>

</template>

<script>
export default {
  name: 'about',
  data: function () {
    return {
      positionX: 0,
      count: 1,
    }
  },
  methods: {
    previous(){
      if(this.count > 1){
        this.positionX += 322+24;
        this.count--;
      }
    },
    next(){
      if (this.count < 3){


      this.positionX = -this.count * (322+24);
      this.count++;
      }

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
  overflow: hidden;
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
  transition: .5s ease;
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
#buttons{
  display: none;
  display: inline-block;
}

@media (max-width: 1385px) {
#program{
  align-items: flex-start;
  padding: 20px;
  overflow: hidden;
}
  p{
    text-align: left;
  }
  a{
    width: 280px;
    text-align: center;
  }

  Button{
    background-color: #1D1D1D;
    border: none;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    cursor: pointer;
    margin-right: 12px;
    transition: .5s ease;
  }
  Button:nth-child(2){
    transform: rotateZ(180deg);
  }

  #buttons{
    position: absolute;
    z-index: 1;
    right: 50%;
    top: 7400px;
    transform: translateX(50px);

  }



}



.notClickable{
  opacity: 0;
  transition: .5s ease;
}
.notClickable svg {
  fill: #1D1D1D;
}


</style>
