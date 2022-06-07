<template>
  <div id="nav">
    <h3>EXPÉRIENCE</h3>
    <div id="container" >
      <a href="#about" class="txt" >LA LIBRAIRIE</a>
      <a href="#love" class="txt">COUPS DE COEUR</a>
      <a href="#program" class="txt">ÉVÉNEMENTS</a>
      <a href="/" class="txt">BOUTIQUE</a>
      <a href="/" class="txt">CONTACT</a>

      <a href="/"  class="svg">
        <svg id="login" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M8 8C10.21 8 12 6.21 12 4C12 1.79 10.21 0 8 0C5.79 0 4 1.79 4 4C4 6.21 5.79 8 8 8ZM8 10C5.33 10 0 11.34 0 14V16H16V14C16 11.34 10.67 10 8 10Z" fill="#1D1D1D"/>
        </svg>
      </a>
      <a href="/" class="svg">
        <svg id="pannier" width="16" height="20" viewBox="0 0 16 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M14 4H12C12 1.79 10.21 0 8 0C5.79 0 4 1.79 4 4H2C0.9 4 0 4.9 0 6V18C0 19.1 0.9 20 2 20H14C15.1 20 16 19.1 16 18V6C16 4.9 15.1 4 14 4ZM6 8C6 8.55 5.55 9 5 9C4.45 9 4 8.55 4 8V6H6V8ZM8 2C9.1 2 10 2.9 10 4H6C6 2.9 6.9 2 8 2ZM12 8C12 8.55 11.55 9 11 9C10.45 9 10 8.55 10 8V6H12V8Z" fill="#1D1D1D"/>
        </svg>

      </a>
      <a href="/" id="loupe" class="svg">
        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M14.2939 12.5786H13.3905L13.0703 12.2699C14.191 10.9663 14.8656 9.27387 14.8656 7.43282C14.8656 3.32762 11.538 0 7.43282 0C3.32762 0 0 3.32762 0 7.43282C0 11.538 3.32762 14.8656 7.43282 14.8656C9.27387 14.8656 10.9663 14.191 12.2699 13.0703L12.5786 13.3905V14.2939L18.2962 20L20 18.2962L14.2939 12.5786ZM7.43282 12.5786C4.58548 12.5786 2.28702 10.2802 2.28702 7.43282C2.28702 4.58548 4.58548 2.28702 7.43282 2.28702C10.2802 2.28702 12.5786 4.58548 12.5786 7.43282C12.5786 10.2802 10.2802 12.5786 7.43282 12.5786Z" fill="#1D1D1D"/>
        </svg>
      </a>

      <a href="" id="burger">
        <svg width="28" height="20" viewBox="0 0 28 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M0 20H28V16.6667H0V20ZM0 11.6667H28V8.33333H0V11.6667ZM0 0V3.33333H28V0H0Z" fill="black"/>
        </svg>
      </a>

    </div>


  </div>
</template>

<script>
export default {
  name: 'nav',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #nav{
    width: 100vw;
    height: 126px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #1D1D1D;
    text-decoration: none;
    background-color: #FFF5E6;
  }
  #container{
    display: flex;
    align-items: center;
    height: 100%;
  }

  a{
    color: #1D1D1D;
    font-size: 24px;
    height: 27px;
    font-weight: 800;
    margin-right: 20px;
    font-family: 'pp_pangram_sansbold';
  }
  .svg  {
    display: inline-block;
    border: solid 1px #1D1D1D;
    border-radius: 50px;
    width: 44px;
    height: 44px;
  }
  .svg svg  {
    display: inline-block;
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  #login    {
    transform: translate(-50%, -80%);
  }
  #burger {
    display: none;
  }
  @media (max-width: 1385px) {
    .txt,
    #loupe  {
      display: none;
    }
    .svg{
      border: none  ;
    }
    #burger {
      display: block;
    }

    span{
      display: inline-block;
      position: absolute;
    }

  }

</style>
