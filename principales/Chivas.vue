<template>
<span >
    <section class="top-0 z-0 h-full max-h-full bg-no-repeat bg-auto bg ">
    <base-header @back-event="backEvent" @pass-event="passEvent"></base-header>
    <div class="flex justify-center w-full">
        <div class="flex justify-center w-full">
        <span class="w-full">

            <div class="flex flex-col">
                <span class="flex justify-center w-full h-48 mt-16">
                    <img src="../static/Principales/chivas/titulo.png" alt="">
                </span>
                <div class="flex flex-row px-32">
                    <span v-gsap.fromTo="[{ y: -700, scale: .75 }, { y: 0, scale:1, duration: 1}]" class="flex justify-center w-1/3 opacity-80 hover:opacity-100">
                        <img @click="passEvent('ChivasExtra')" class="cursor-pointer grow" src="../static/Principales/chivas/izquierda.png" alt="">
                    </span>
                    <span v-gsap.fromTo="[{ y: -700, scale: .75 }, { y: 0, scale:1, duration: 1.5}]"  class="flex justify-center w-1/3 opacity-80 hover:opacity-100">
                        <img @click="passEvent('Chivas12')" class="cursor-pointer grow" src="../static/Principales/chivas/central.png" alt="">
                    </span>
                    <span v-gsap.fromTo="[{ y: -700, scale: .75 }, { y: 0, scale:1, duration: 1.5}]"  class="flex justify-center w-1/3 opacity-80 hover:opacity-100">
                        <img @click="passEvent('ChivasTequila')" class="cursor-pointer grow" src="../static/Principales/chivas/derecha.png" alt="">
                    </span>
                </div>
            </div>
        </span>
    </div>
    </div>
    </section>
</span>
</template>

<script>
import BaseHeader from '../components/BaseHeader.vue';
import PrincipalesTres from './PrincipalesTres.vue';
import Principales from './Principales.vue';

export default {
components:{
      BaseHeader,
      PrincipalesTres,
      Principales
    },
methods: {
    passEvent(event)
    {
      this.$emit('pass-event', event)
    },
    backEvent(event)
    {
      this.$emit('pass-event', PrincipalesTres)
    },
  }
};
</script>
