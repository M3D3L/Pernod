<template>

<section :style="image" class="top-0 left-0 h-screen bg-center bg-auto">
    <div  class="flex w-full ">
        <span class="flex justify-center w-full ">

            <img v-gsap.fromTo="[{ y: -700 }, { y: 0,  duration: 1.25}]" class="relative transform scale-75"  src="../static/Infografias/AbsolutSabores/contenido.png" alt="">
            <base-header class="absolute w-full" @pass-event="passEvent" @back-event="backEvent"></base-header></spa>
        </span>
      <span v-gsap.fromTo="[{ x: 700 }, { x: 0,  duration: 1.25}]" class="absolute flex justify-end w-4/5 bottom-20 ">
      <span class="flex flex-row h-40">
        <span >
        </span>
        <img class="cursor-pointer grow opacity-70 hover:opacity-100" @click="passEvent('CoctelCitron')" src="../static/Principales/absolut/central1.png" alt="">
        <img class="cursor-pointer grow opacity-70 hover:opacity-100" @click="passEvent('CoctelMandarin')" src="../static/Principales/absolut/central2.png" alt="">
        <img class="cursor-pointer grow opacity-70 hover:opacity-100" @click="passEvent('CoctelLime')" src="../static/Principales/absolut/central3.png" alt="">
        <img class="cursor-pointer grow opacity-70 hover:opacity-100" @click="passEvent('CoctelRaspberri')" src="../static/Principales/absolut/central4.png" alt="">
      </span>

      </span>
    </div>
    </section>
</template>

<script>
import BaseHeader from "../components/BaseHeader.vue";
import Absolut from "../Principales/Absolut.vue";
import bgImg from "../static/Infografias/AbsolutSabores/fondo.png"

export default {
  components: {
    BaseHeader,
    Absolut,
    bgImg
  },
  data() {
    return {
      image: { backgroundImage: `url(${bgImg})` },
    };
  },
  methods: {
    passEvent(event)
    {
      this.$emit('pass-event', event )
    },
    backEvent(event)
    {
      this.$emit('pass-event', Absolut)
    },
  }
};
</script>
