<template>
    <section class="flex flex-col w-full">
      <base-header class="w-full" @back-event="backEvent" @pass-event="passEvent"></base-header>
        <span class="w-full pt-8">
                <span class="flex justify-center w-full h-40 mt-8">
                    <img src="../static/Principales/principalTres/Título.png" alt="">
                </span>
                <div v-gsap.fromTo="[{ y: -400 }, {  y:0, duration: .5}]" class="flex justify-center px-16 mt-32 space-x-4" >

                    <span  class="flex flex-col w-1/12">
                      <div  class="flex justify-center w-full tracking-tighter text-center opacity-80 h7">CHAMPAGNE</div>
                      <hr class="w-4/5 mx-auto mt-8 border-2">
                      <span class="flex flex-row mt-16">
                      <span class="flex justify-center w-full h-72" @click="passEvent('Mumm')">
                        <img  class="cursor-pointer grow opacity-80 hover:opacity-100" src="../static/Principales/Botellas/mumm.png" alt="champagne">
                    </span>
                    </span>
                    </span>

                    <span  class="flex flex-col w-1/12">
                      <h6 class="flex justify-center w-full text-center opacity-80 neon-text">LICOR</h6>
                      <hr class="w-4/5 mx-auto mt-8 border-2">
                      <span class="flex flex-row mt-16">
                      <span class="flex justify-center w-full h-72" >
                        <img  class="cursor-pointer grow opacity-80 hover:opacity-100" src="../static/Principales/Botellas/Malibu.png" alt="licor">
                    </span>
                    </span>
                    </span>

                    <span  class="flex flex-col w-1/12">
                      <h4 class="flex justify-center w-full text-center transform opacity-80 hue-rotate-30">RON</h4>
                      <hr class="w-4/5 mx-auto mt-8 border-2">
                      <span class="flex flex-row mt-16">
                      <span class="flex justify-center w-full h-72" @click="passEvent('HavanaClub7')">
                        <img id="eight" class="cursor-pointer grow opacity-80 hover:opacity-100" src="../static/Principales/Botellas/Havana.png" alt="cognac">
                    </span>

                    </span>
                    </span>

                    <span  class="flex flex-col w-1/6">
                      <h4  class="flex justify-center w-1/2 mx-auto text-center opacity-80">GINEBRA</h4>
                      <hr class="w-4/5 mx-auto mt-8 border-2">
                      <span class="flex flex-row mt-16">
                      <span class="flex justify-center w-1/2 h-72" @click="passEvent('Monkey')">
                        <img id="eight" class="flex justify-center mt-12 cursor-pointer grow opacity-80 hover:opacity-100" src="../static/Principales/Botellas/Monkey.png" alt="cognac">
                      </span>
                      <span class="flex justify-center w-1/2 h-72" @click="passEvent('BeefEater')">
                        <img id="eight" class="w-3/5 cursor-pointer grow opacity-80 hover:opacity-100" src="../static/Principales/Botellas/Beefeater.png" alt="cognac">
                      </span>
                    </span>
                    </span>

                    <span  class="flex flex-col w-1/3">
                      <h5  class="flex justify-center w-1/3 mx-auto">Whiskey</h5>
                      <hr class="w-4/5 mx-auto mt-8 mb-16 border-2">
                      <span class="flex flex-row w-full">

                      <span class="flex justify-center w-1/4" @click="passEvent('Chivas')">
                        <img id="eight" class="cursor-pointer grow opacity-80 hover:opacity-100 h-72" src="../static/Principales/Botellas/Chivas12.png"  alt="cognac">
                      </span>
                      <span class="flex justify-center w-1/4" @click="passEvent('TheGlenLivet')">
                        <img id="eight" class="cursor-pointer grow opacity-80 hover:opacity-100 h-72" src="../static/Principales/Botellas/TGL.png"  alt="cognac">
                      </span>
                      <span class="flex justify-center w-1/4" @click="passEvent('Jameson')">
                        <img id="eight" class="cursor-pointer grow opacity-80 hover:opacity-100 h-72" src="../static/Principales/Botellas/Jameson.png"  alt="cognac">
                      </span>
                      <span class="flex justify-center w-1/4" @click="passEvent('Ballantines')">
                        <img id="eight" class="w-4/5 mt-12 cursor-pointer grow opacity-80 hover:opacity-100 h-60" src="../static/Principales/Botellas/Ballantines.png"  alt="cognac">
                      </span>
                    </span>
                    </span>

                    <span  class="flex flex-col w-1/12">
                      <div  class="flex justify-center w-full text-center opacity-80 h8">VODKA</div>
                      <hr class="w-4/5 mx-auto mt-8 border-2">
                      <span class="flex flex-col justify-center w-full" @click="passEvent('Absolut')">

                        <img id="eight" class="w-4/5 mx-auto mt-16 cursor-pointer grow opacity-80 hover:opacity-100 h-72" src="../static/Principales/Botellas/Absolut.png" alt="vodka">
                    </span>
                    </span>

                    <span  class="flex flex-col w-1/12">
                      <div  class="flex justify-center w-full text-center opacity-80 h8">Tequila</div>
                      <hr class="w-4/5 mx-auto mt-8 border-2">
                      <span class="flex flex-col justify-center w-full" @click="passEvent('Altos')">

                        <img id="eight" class="w-4/5 mx-auto mt-16 cursor-pointer grow opacity-80 hover:opacity-100 h-72" src="../static/Principales/Botellas/Altos.png" alt="cognac">
                    </span>
                    </span>

                    <span  class="flex flex-col w-1/12">
                      <h3  class="flex justify-center w-full text-center opacity-80">Cognac</h3>
                      <hr class="w-4/5 mx-auto mt-8 border-2">
                      <span class="flex flex-col justify-center w-full" @click="passEvent('Martell')">

                        <img id="eight" class="w-4/5 mx-auto mt-16 cursor-pointer grow opacity-80 hover:opacity-100 h-72" src="../static/Principales/Botellas/BlueSwift.png" alt="cognac">
                    </span>
                    </span>

            </div>
        </span>
    </section>



</template>

<script>
import BaseHeader from '../components/BaseHeader.vue'
import Formulario from '../principales/Formulario.vue';

export default {
  components:{
      BaseHeader,
    },
  methods: {
    passEvent(event)
    {
      this.$emit('pass-event', event)

    },
    backEvent(event)
    {
      this.$emit('pass-event', Formulario)

    },

  }
};
</script>

<style scoped>

h3, h4, h5, h6, .h7, .h8 {
  animation: pulsate 0.11s ease-in-out infinite alternate, flicker 3s ease-in-out infinite alternate;
padding: 0.4em;
background-color: transparent;
font-size: x-large;
animation: pulsate 0.11s ease-in-out infinite alternate, flicker 3s ease-in-out infinite alternate;
border: 0.2rem solid #fff;
border-radius: 2rem;
color: white;
padding: 0.4em;
background-color: transparent;
}
  h3 {
box-shadow: 0 0 .2rem #fff,
            0 0 .2rem #fff,
            0 0 2rem #1398fe,
            0 0 0.8rem #134afe,
            0 0 2.8rem #1323fe,
            inset 0 0 1.3rem #1336fe;
}

h4 {
box-shadow: 0 0 .2rem #fff,
            0 0 .2rem #fff,
            0 0 2rem #fe4a13,
            0 0 0.8rem #fe2313,
            0 0 2.8rem #fe1313,
            inset 0 0 1.3rem #fe1b13;
}

h5 {

box-shadow: 0 0 .2rem #fff,
            0 0 .2rem #fff,
            0 0 2rem #27fe13,
            0 0 0.8rem #0fa71c,
            0 0 2.8rem #03661f,
            inset 0 0 1.3rem #013010;
}

h6 {

box-shadow: 0 0 .2rem #fff,
            0 0 .2rem #fff,
            0 0 2rem #ea13fe,
            0 0 0.8rem #9f0fa7,
            0 0 2.8rem #66035a,
            inset 0 0 1.3rem #30012a;
}
.h7 {
box-shadow: 0 0 .2rem #fff,
            0 0 .2rem #fff,
            0 0 2rem #fe4a13,
            0 0 0.8rem #e05408,
            0 0 2.8rem #febb13,
            inset 0 0 1.3rem #fedb13;
}

  .h8 {
box-shadow: 0 0 .2rem #fff,
            0 0 .2rem #fff,
            0 0 2rem #1398fe,
            0 0 0.8rem #1379fe,
            0 0 2.8rem #13d3fe,
            inset 0 0 1.3rem #13fefe;
}
</style>
