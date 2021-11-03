<template>
<span >
    <section class="top-0 z-0 h-full max-h-full bg-no-repeat bg-auto bg ">
    <base-header @back-event="backEvent" @pass-event="passEvent"></base-header>
    <div class="flex justify-center w-full">
        <div class="flex justify-center w-full">
        <span class="w-full">

            <div class="flex flex-col">
                <span class="flex justify-center w-full h-48 mt-16">
                    <img src="../static/Principales/monkey/titulo.png" alt="">
                </span>
                <div class="flex flex-row px-32">
                    <span v-gsap.fromTo="[{ y: -700, scale: .75 }, { y: 0, scale:1, duration: 1}]" class="flex justify-center w-1/2 opacity-80 hover:opacity-100">
                        <img @click="passEvent('MonkeyDryGin')" class="cursor-pointer grow" src="../static/Principales/monkey/izquierda.png" alt="">
                    </span>
                    <span v-gsap.fromTo="[{ y: -700, scale: .75 }, { y: 0, scale:1, duration: 1.5}]"  class="flex justify-center w-1/2 opacity-80 hover:opacity-100">
                        <img @click="passEvent('MonkeySloeGin')" class="cursor-pointer grow" src="../static/Principales/monkey/derecha.png" alt="">
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
import PrincipalesTres from '../principales/PrincipalesTres.vue';
import Principales from '../principales/Principales.vue';

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
