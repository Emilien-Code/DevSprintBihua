<template>
  <HelloWorld/>
    <Main/>
    <Caroussel/>
    <About/>
  <WeLove/>
  <AskProgram/>
  <Footer />
</template>

<script>
import HelloWorld from './components/nav.vue'
import Main from "./components/main";
import Caroussel from "./components/caroussel";
import About from "./components/about";
import WeLove from "./components/weLove";
import AskProgram from "./components/askProgram";
import Footer from "./components/footer";
export default {
  name: 'App',
  components: {
    HelloWorld,
    Main,
    Caroussel,
    About,
    WeLove,
    AskProgram,
    Footer,
  }
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}
#app {
  scroll-behavior: smooth;
}
span{
  font-family: pp_neue_montrealmedium;
}
a{
  text-decoration: none;
  font-family: pp_neue_montrealmedium;
}
p{
  font-size: 20px;
  font-family: pp_neue_montrealmedium;
}
h4  {
  font-family: 'pp_pangram_sansbold';
  font-style: normal;
  font-weight: 800;
  font-size: 40px;
  line-height: 48px;
}
h3{
  font-size: 60px;
  font-family: 'pp_pangram_sansbold';

}
h2{
  font-size: 120px;
  font-family: 'pp_pangram_sansbold';

}
h1{
  font-family: 'pp_pangram_sansbold';
  font-style: normal;
  font-weight: 800;
  font-size: 200px;
  line-height: 228px;
}

@media (max-width: 1385px) {
  h4  {
    font-family: 'pp_pangram_sansbold';
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 32px;
  }
  h3{
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 32px;

    font-family: 'pp_pangram_sansbold';

  }
  h2{
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 32px;
    font-family: 'pp_pangram_sansbold';

  }
  h1{
    font-family: 'pp_pangram_sansbold';
    font-style: normal;
    font-weight: 800;
    font-size: 60px;
    line-height: 68px;
  }
}





@font-face {
  font-family: 'pp_pangram_sansbold';
  src: url('./assets/Font/Pangram/pppangramsans-bold-webfont.woff2') format('woff2'),
  url('./assets/Font/Pangram/pppangramsans-bold-webfont.woff') format('woff');
  font-weight: 800;
  font-style: normal;
}



@font-face {
  font-family: 'pp_neue_montrealmedium';
  src: url('./assets/Font/NeueMontreal/ppneuemontreal-medium-webfont.woff2') format('woff2'),
  url('./assets/Font/NeueMontreal/ppneuemontreal-medium-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}
</style>
