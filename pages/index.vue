
<template>
    <div :style="image"  class="top-0 left-0 h-screen bg-center bg-no-repeat bg-auto" >
        <component :is="component" class="relative w-full" @pass-event="togglePageChange"/>
        <span>
        </span>
    </div>
</template>

<script>
import BaseHeader from '../components/BaseHeader.vue'
import Principales from '../principales/Principales.vue'
import PrincipalesDos from '../principales/PrincipalesDos.vue'
import Formulario from '../principales/Formulario.vue'
import PrincipalesTres from '../principales/PrincipalesTres.vue'
import Absolut from '../principales/Absolut.vue'
import Martell from '../principales/Martell.vue'
import Chivas from '../principales/Chivas.vue'
import Monkey from '../principales/Monkey.vue'
import BeefEater from '../principales/Beefeater.vue'
import Altos from '../infografias/Altos.vue'
import Mumm from '../infografias/Mumm.vue'
import TheGlenLivet from '../infografias/TheGlenLivet.vue'
import MonkeySloeGin from '../infografias/MonkeySloeGin.vue'
import MonkeyDryGin from '../infografias/MonkeyDryGin.vue'
import HavanaClub7 from '../infografias/HavanaClub7.vue'
import BeefEaterPink from '../infografias/BeefEaterPink.vue'
import BeefEaterLondon from '../infografias/BeefEaterLondon.vue'
import BeefEaterBlackberry from '../infografias/BeefEaterBlackberry.vue'
import ChivasExtra from '../infografias/ChivasExtra.vue'
import Chivas12 from '../infografias/Chivas12.vue'
import ChivasTequila from '../infografias/ChivasTequila.vue'
import Jameson from '../infografias/Jameson.vue'
import Ballantines from '../infografias/Ballantines.vue'
import AbsolutBlue from '../infografias/AbsolutBlue.vue'
import AbsolutExtrakt from '../infografias/AbsolutExtrakt.vue'
import AbsolutSabores from '../infografias/AbsolutSabores.vue'
import MartellVSOP from '../infografias/MartellVSOP.vue'
import MartellBlueSwift from '../infografias/MartellBlueSwift.vue'
import CoctelRaspberri from '../cocteles/CoctelRaspberri.vue'
import CoctelPink from '../cocteles/CoctelPink.vue'
import CoctelMonkeySloeGin from '../cocteles/CoctelMonkeySloeGin.vue'
import CoctelMonkeyDryGin from '../cocteles/CoctelMonkeyDryGin.vue'
import CoctelMartellVSOP from '../cocteles/CoctelMartellVSOP.vue'
import CoctelMandarin from '../cocteles/CoctelMandarin.vue'
import CoctelLondon from '../cocteles/CoctelLondon.vue'
import CoctelLime from '../cocteles/CoctelLime.vue'
import CoctelJameson from '../cocteles/CoctelJameson.vue'
import CoctelHavanaClub7 from '../cocteles/CoctelHavanaClub7.vue'
import CoctelExtrakt from '../cocteles/CoctelExtrakt.vue'
import CoctelCitron from '../cocteles/CoctelCitron.vue'
import CoctelChivasTequila from '../cocteles/CoctelChivasTequila.vue'
import CoctelChivasSherry from '../cocteles/CoctelChivasSherry.vue'
import CoctelChivas from '../cocteles/CoctelChivas.vue'
import CoctelBlueSwift from '../cocteles/CoctelBlue.vue'
import CoctelBlue from '../cocteles/CoctelBlue.vue'
import CoctelBlackBerry from '../cocteles/CoctelBlackBerry.vue'
import CoctelBallantines from '../cocteles/CoctelBallantines.vue'
import CoctelAltos from '../cocteles/CoctelAltos.vue'
import bgImg from "../static/principales/Fondo.png"

export default {
  components: {
  BaseHeader,
  Principales,
  PrincipalesDos,
  Formulario,
  PrincipalesTres,
  Mumm,
  TheGlenLivet,
  MonkeySloeGin,
  MonkeyDryGin,
  Martell,
  Absolut,
  Chivas,
  BeefEater,
  Monkey,
  Altos,
  BeefEaterPink,
  BeefEaterLondon,
  BeefEaterBlackberry,
  ChivasExtra,
  Chivas12,
  ChivasTequila,
  Jameson,
  Ballantines,
  AbsolutBlue,
  AbsolutExtrakt,
  AbsolutSabores,
  MartellVSOP,
  MartellBlueSwift,
  HavanaClub7,
  CoctelRaspberri,
  CoctelPink,
  CoctelMonkeySloeGin,
  CoctelMonkeyDryGin,
  CoctelMartellVSOP,
  CoctelMandarin,
  CoctelLondon,
  CoctelLime,
  CoctelJameson,
  CoctelHavanaClub7,
  CoctelExtrakt,
  CoctelCitron,
  CoctelChivasTequila,
  CoctelChivasSherry,
  CoctelChivas,
  CoctelBlueSwift,
  CoctelBlue,
  CoctelBlackBerry,
  CoctelBallantines,
  CoctelAltos,

  },
  data() {
    return {
      image: { backgroundImage: `url(${bgImg})` },
      component:
      Principales
  }
  },
  methods: {
    togglePageChange(event) {
      this.component= event;

    },

},
}
</script>

<style>
.grow { transition: all .2s ease-in-out; }
.grow:hover { transform: scale(1.1); }


.neonText {
color: #fff;
text-shadow:
    0 0 7px #fff,
    0 0 10px #fff,
    0 0 21px #fff,
    0 0 42px #0fa,
    0 0 82px #0fa,
    0 0 92px #0fa,
    0 0 102px #0fa,
    0 0 151px #0fa;
    animation: pulsate 1.75s infinite alternate;
    animation: flicker 2.5s infinite alternate;
}

/* Flickering animation */
@keyframes flicker {

  0%, 18%, 22%, 25%, 53%, 57%, 100% {

      text-shadow:
      0 0 4px #fff,
      0 0 11px #fff,
      0 0 19px #fff,
      0 0 40px #0fa,
      0 0 80px #0fa,
      0 0 90px #0fa,
      0 0 100px #0fa,
      0 0 150px #0fa;

  }

  20%, 24%, 55% {
      text-shadow: none;
  }
}


@keyframes pulsate {
  100% {
    /* Larger blur radius */
    text-shadow:
      0 0 4px #fff,
      0 0 11px #fff,
      0 0 19px #fff,
      0 0 40px #f09,
      0 0 80px #f09,
      0 0 90px #f09,
      0 0 100px #f09,
      0 0 150px #f09;
  }
0% {
    /* A slightly smaller blur radius */
    text-shadow:
      0 0 4px #fff,
      0 0 10px #fff,
      0 0 18px #fff,
      0 0 38px #f09,
      0 0 73px #f09,
      0 0 80px #f09,
      0 0 94px #f09,
      0 0 140px #f09;
  }
}


h1 {
animation: pulsate 0.11s ease-in-out infinite alternate, flicker 3s ease-in-out infinite alternate;
border: 0.2rem solid #fff;
border-radius: 2rem;
padding: 0.4em;

}

input, h1, select {
border: 0.2rem solid #fff;
border-radius: 2rem;
background-color: transparent;
box-shadow: 0 0 .2rem #fff,
            0 0 .2rem #fff,
            0 0 2rem #bc13fe,
            0 0 0.8rem #bc13fe,
            0 0 2.8rem #bc13fe,
            inset 0 0 1.3rem #bc13fe;
}

h2, input, h1, select{
animation: pulsate 0.11s ease-in-out infinite alternate, flicker 3s ease-in-out infinite alternate;
padding: 0.4em;
color: white;
font-size: x-large;
}

body {
    overflow: hidden; /* Hide scrollbars */
}


body {
    overflow: hidden; /* Hide scrollbars */
}

</style>
